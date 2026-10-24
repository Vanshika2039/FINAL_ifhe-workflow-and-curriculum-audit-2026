# Task 1 — College workflow investigation and redesign

**Prepared:** 24 October 2026  
**Status:** Simulated proposal due to unavailable access; not field-validated.

## 1. Scope and ethical boundary
I could not access a real college workflow or obtain permission to observe staff/student transactions before the deadline. To avoid inventing fieldwork, this report uses a **hypothetical academic-document request workflow** as a design scenario. It is not asserted to be IFHE's actual procedure. No real personal records are used. The proposed workflow should be validated with a process owner before adoption.

## 2. Problem statement
A generic email/chat-based request process can become difficult to track if required fields are missing, duplicate requests are submitted, approval authority is unclear, or a handoff is missed. These are plausible failure modes for many request workflows, but their occurrence and frequency at IFHE are **unverified assumptions**.

**Hypothesis to test:** A single request form with a unique tracking ID, explicit statuses, required-field checks, role-based approval and a recovery queue can reduce avoidable follow-up work and make ownership visible.

## 3. Baseline process map (hypothetical)
1. Student identifies a need and sends a request.
2. Receiver checks whether the request has enough information.
3. If information is missing, receiver asks for correction; request waits.
4. Complete request is routed to the designated reviewer.
5. Reviewer approves, rejects, or asks for clarification.
6. Fulfilment owner completes the permitted action.
7. Student receives outcome and the record is closed.

### Handoffs and exceptions
- Student → intake/administrative receiver: submission.
- Receiver → authorized approver: review.
- Approver → fulfilment owner: approved action.
- Fulfilment owner → requester: completion or failure notice.
- Exceptions: missing details, duplicate request, unauthorized requester, rejection, service/system failure, and no response from an owner.

This is a proposed generic map, not an observed IFHE process.

## 4. Evidence log and classification
See `evidence-log.csv`. Published-source facts are separated from assumptions and synthetic examples. Since no field access was available, there are no observed facts about actual IFHE workflow timings or volume. A next-stage investigator should request permission, document the process owner's consent, observe only the minimum necessary steps, and avoid collecting personal data.

## 5. Proposed improved process
### Inputs
- Request type (allowlisted values)
- Non-sensitive reference needed to fulfil the request (avoid student ID in public/test data)
- Description and required attachments, if applicable
- Requester role and contact channel (kept only in an approved private system; never in this public demo)
- Submission timestamp and generated request ID

### Status model
`DRAFT → SUBMITTED → VALIDATING → NEEDS_INFO → READY_FOR_REVIEW → APPROVED / REJECTED → IN_PROGRESS → COMPLETED`

Additional terminal/recovery statuses: `DUPLICATE_LINKED`, `UNAUTHORIZED`, `FAILED_RETRY`, `CANCELLED`, `ESCALATED`.

### Ownership and approval boundaries
- **Accountable owner:** designated process owner (role to be assigned by the institution).
- **Intake handler:** checks completeness and routes; cannot approve their own request unless policy explicitly permits it.
- **Approver:** only the role formally authorized for that request type can approve/reject.
- **Fulfilment owner:** performs only the action covered by approval.
- **Requester:** may correct missing fields and view status; cannot change approval outcome.
- Any exception outside policy is paused and escalated; the workflow does not infer approval.

### Fallback and recovery
- If a required field is missing, move to `NEEDS_INFO`; state exactly what is missing and retain the same request ID.
- If a likely duplicate is detected, do not silently delete it. Link to the existing request and ask the owner to confirm.
- If requester authority cannot be verified, move to `UNAUTHORIZED` and route to a human owner; do not reveal restricted information.
- If fulfilment fails, record a non-sensitive error category, move to `FAILED_RETRY`, allow one controlled retry, then escalate to the process owner.
- If the system is unavailable, use a pre-approved manual fallback and reconcile the record when service returns. Do not use personal messaging accounts or unapproved storage.
- Preserve a minimal audit trail: status, timestamp, role, action, reason code. Retention and access rules must be set by the institution.

## 6. Five synthetic tests
See `test-cases.csv` for inputs, expected results, and recovery. All five cases are synthetic and were designed as acceptance tests; they are not real student cases.

## 7. Impact estimate
Illustrative assumptions are provided in `calculations.md`. The estimates are a planning model, not measured impact. A real pilot should measure median handling time, number of follow-ups, rework, failed fulfilments, and support burden for a defined period before and after the change.

## 8. Pilot and evaluation
1. Obtain written permission from the process owner.
2. Map the actual current state with the owner and one or more consenting participants.
3. Confirm required fields, policy, authorized approver roles, fallback and retention.
4. Run synthetic tests before any live pilot.
5. Pilot only with consent and minimal permitted data.
6. Compare time per completed request, missing-field rate, duplicate rate, escalation rate and requester satisfaction.
7. Keep a rollback/manual process and stop if privacy or authorization issues appear.

## 9. Limitation and personal contribution
I could not verify that this workflow exists at IFHE or obtain staff/faculty feedback. The map, failure modes and proposed system are design hypotheses. The submission must not be read as evidence of current institutional practice. Personal contribution should be described accurately in the top-level README.
