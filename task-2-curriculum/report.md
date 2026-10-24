# Task 2 — B.Tech CSE Curriculum Audit and Redesign

## 1. Objective

This audit evaluates the reported curriculum of the B.Tech Computer Science and Engineering programme for the 2023–2027 admission cohort at ICFAI Tech, IFHE Hyderabad. It identifies curriculum strengths, potential improvements for current analytics-related roles, opportunities for responsible AI-assisted learning, and a proposed practical capstone.

The aim is to improve industry relevance without removing foundational computer science knowledge or assuming that unverified changes comply with university regulations.

## 2. Evidence and Scope

### Sources Used

- Student portal: course codes and credits supplied by a student from the 2023–2027 cohort.
- Official IFHE programme structure: https://ifheindia.org/icfai-tech-school-hyderabad/icfaitech-btech-program-structure
- Official B.Tech CSE programme page: https://www.ifheindia.org/icfaitech-school-hyderabad/icfaitech/ugprograms/btech-cse
- Three job descriptions recorded in `job-description-comparison.csv`.
- AI exercise and verification records maintained in `ai-verification-log.csv`.

The public programme structure does not match the complete course list supplied for this cohort. The exact cohort-specific regulations and official syllabus were not located publicly. Therefore, the student-provided course map is used as working evidence, not as an independently verified official curriculum.

## 3. Course and Credit Summary

| Semester | Reported credits |
|---|---:|
| Semester 1 | 20 |
| Semester 2 | 24 |
| Semester 3 | 23 |
| Semester 4 | 24 |
| Semester 5 | 24 |
| Semester 6 | 21 |
| **Semesters 1–6** | **136** |
| Semester 7 | 15 |
| **Semesters 1–7** | **151** |

These totals are calculated from the credits supplied from the student portal.

In this student's Semester 7 pathway, CS415 Ethical Hacking and DS401 Human Computer Interaction are college courses. OE418 Foundations for Virtual and Augmented Reality Systems, OE707 Business Intelligence & Analytics, and OE800 Education for Sustainable Development are NPTEL-transferred courses. Other students may complete the elective requirements through different combinations of college and NPTEL courses.

The transferred courses are included in the reported Semester 7 total; they are not additional credits on top of it.

Semester 8 is reported as an internship semester. Its credit value, any accompanying courses, and the applicable official requirements remain unverified.

## 4. Curriculum Audit: KEEP, UPDATE, REDUCE and ADD

The following are proposed content and learning-outcome recommendations. They are not claims that the university has approved changes to its curriculum.

### KEEP

1. **CS206 — Database Management Systems:** Retain relational modelling, SQL, joins, aggregation, subqueries and transaction concepts. These form a useful foundation for analytics.
2. **DS202 — Industry Coding Practice (Python/R):** Retain practical programming and data-manipulation exercises.
3. **DS203 — Data Science:** Retain data preparation, exploratory analysis and interpretation of results.
4. **DS304 — Machine Learning:** Retain model selection, evaluation and limitations.
5. **DS201 — Artificial Intelligence:** Retain foundational AI concepts while distinguishing them from data science and machine learning.
6. **CS304 — Software Engineering:** Retain requirements analysis, testing, version control and team-based development.
7. **CS307 — Cloud Computing:** Retain cloud architecture and deployment fundamentals.
8. **DS307 — Big Data Systems:** Retain scalable data processing and data-system concepts.

### UPDATE

9. **Database and programming practicals:** Use realistic, synthetic business datasets, data-quality checks and multi-table analysis. Assess correctness, readability and explanation, not just whether code runs.

10. **Data Science and Machine Learning:** Require students to document missing values, data leakage risks, train/test separation, appropriate metrics and model limitations.

11. **Software Engineering and project assessment:** Include Git-based collaboration, meaningful commits, README documentation, test cases and reproducible setup instructions.

12. **Business Intelligence & Analytics and HCI:** Include dashboard design, metric definitions, accessibility, user feedback and explanation of how a decision-maker should interpret a result.

### REDUCE

Reduce repetitive, disconnected exercises where students repeatedly perform the same technique without explaining its purpose. Replace some repetition with integrated assignments that require data cleaning, SQL, visualisation, testing and interpretation.

This recommendation concerns duplicated learning activities, not removal of compulsory courses or reduction of course credits.

### ADD

Introduce or formally strengthen the following learning outcomes within suitable existing courses, subject to programme approval:

- Data quality, validation and responsible handling of information.
- Practical spreadsheet and BI dashboard evaluation.
- API and workflow integration.
- AI-assisted coding with independent verification.
- Reproducibility, documentation and communicating uncertainty.
- Testing automated workflows, including failure recovery and access-control checks.

## 5. Job-Description Comparison

Use `job-description-comparison.csv` to compare three job postings:

- Citi — Business Analytics with Python and SQL.
- Jio — Associate Business Analyst.
- Cummins — Business Intelligence Analyst.

For each posting, record the exact title, employer, working URL, date accessed, displayed posting date if available, required skills, preferred skills and evidence supporting each entry.

The Citi role is recorded as requiring prior data analytics experience: a bachelor's degree plus three or more years of experience, or a master's degree plus two or more years. It is therefore not an entry-level role. It is included as a reference for the skills used in business analytics positions, not as evidence that the role is suitable for a fresher.

Job availability and displayed posting details should be reconfirmed on the employer's official page at submission time. The recorded posting date and access date should be retained as evidence of when the listing was reviewed.

The comparison should distinguish explicitly stated requirements from inferred curriculum implications. Do not state that an employer requires a skill unless the listing supports that claim.

The purpose of the comparison is to identify repeated skills across the three postings and determine whether existing courses provide sufficient practical evidence of those skills. A job title alone is not sufficient evidence of its requirements.

## 6. Responsible AI-Assisted Learning

Five exercises are documented in `ai-verification-log.csv`:

1. **CS206 — Database Management Systems:** Use a clearly labelled synthetic employee table to generate an Oracle SQL query that groups employees by department, filters groups using `HAVING`, and calculates average salary.
2. **Probability & Statistics:** Calculate the mean, median and range of the synthetic values 2, 4, 4, 6 and 9.
3. **Software Engineering:** Design a state machine for a generic request workflow and provide five acceptance tests covering normal, missing-information, duplicate, unauthorized and failed-step cases.
4. **Machine Learning:** Explain data leakage with a synthetic train/test example and recommend a leakage-safe evaluation sequence without claiming an unperformed model experiment.
5. **Computer Networks:** Explain TCP and UDP differences, identify relevant authoritative references, and verify core protocol claims.

The log records the prompts, AI tool/model name, date, output excerpts, verification methods, results and evidence status.

The DBMS query was recorded as executed in Oracle SQL*Plus, and the Probability & Statistics calculations were checked manually. The Software Engineering and Machine Learning outputs were reviewed against their stated criteria. The Computer Networks explanation was reviewed and its core protocol claims were cross-checked against official IETF RFC documentation, as recorded in the log.

These checks support the specific results documented, but do not constitute formal validation of every possible AI output. Any corrections or limitations identified during verification should remain documented.

AI-generated material is a starting point, not an authority. Students remain responsible for correctness, citations, privacy and explaining their work independently.

## 7. Proposed Curriculum Change and Credit Impact

The provisional redesign prioritises practical improvements within existing courses before proposing new standalone requirements. This minimises disruption to prerequisites, programme balance and graduation planning.

The mapped Semesters 1–7 contain 151 reported credits. A provisional review target of 33 credits would touch approximately 21.9% of that mapped total.

Calculation:

- Mapped credits for Semesters 1–7: 151.
- Provisional credits targeted for review: 33.
- Percentage: \(33 \div 151 \times 100 \approx 21.9\%\).

This is a planning estimate only. It does **not** establish that 20–25% of the complete degree has been affected, nor does it mean that 33 credits are being added or removed. The specific course-level credit changes and their approval status must be defined before the percentage can be treated as a final result.

The full programme credit requirement, Semester 8 credit value, compulsory/elective rules, prerequisites and cohort-specific regulations have not been independently verified. Consequently, the final percentage of programme credits affected and the degree-credit balance cannot yet be certified.

Before any formal implementation, the department should validate the proposal against the applicable regulations and confirm that prerequisites, compulsory requirements, elective substitutions, internship requirements and graduation totals remain satisfied.

## 8. Proposed Workflow Capstone

### Title: College Academic Request Tracker

Build a prototype for a fictional academic-document request process, such as a student requesting a bonafide certificate.

The prototype should include:

- A structured request form with required-field validation.
- A unique request ID and duplicate-submission detection.
- Explicit statuses: Draft, Submitted, Under Review, Awaiting Information, Approved, Rejected and Completed.
- An accountable owner for each workflow stage.
- Approval permissions that prevent unauthorised users from approving requests.
- An audit log recording status changes.
- Notifications or a visible message when information is missing.
- Recovery instructions for failed steps, without falsely marking a request complete.

Use synthetic records only. This is a proposed simulation, not a claim that the actual college workflow has been observed.

### Required Tests

1. **Normal request:** Valid information moves through the expected stages.
2. **Missing information:** Submission is blocked or routed to Awaiting Information.
3. **Duplicate request:** A repeated submission is detected and handled consistently.
4. **Unauthorised approval:** The action is rejected and logged.
5. **Failed step:** The workflow preserves its state, reports the failure and permits a safe retry or manual escalation.

Record expected results, actual results and evidence in `task-1-workflow/test-cases.csv` where appropriate. The tests should be labelled synthetic unless they are performed against a prototype, in which case the actual results should be recorded separately.

### Evaluation

Measure baseline time and proposed-process time using clearly labelled assumptions or timed prototype tests. Include review and support time, and account for failed requests and recovery.

Do not claim real institutional time savings unless actual observations and sufficient sample evidence support the estimate.

## 9. Feedback and Validation

No faculty or graduate feedback is claimed at this stage. If voluntary feedback can be obtained before submission, record the role of the respondent, the date, the question asked and a consent-respecting summary without unnecessary personal information.

If feedback cannot be obtained, report that limitation honestly.

## 10. Limitations and Next Steps

1. The exact official 2023–2027 syllabus and regulations remain unavailable.
2. Course names and credits are based on student-provided portal information.
3. Semester 8 internship credits and other requirements require confirmation.
4. Job-description details and availability should be reconfirmed against the actual employer postings.
5. AI exercise results are limited to the specific outputs and verification methods recorded in `ai-verification-log.csv`.
6. The proposed workflow is a simulation unless a real process is observed with permission.
7. The proposed credit-impact percentage is provisional and cannot be treated as a final degree-level compliance calculation.

The remaining steps are to reconfirm job-posting details and availability, test the interactive course-comparison tool, check consistency across the reports and CSV files, review privacy and source links, and validate the repository before release. The official cohort-specific curriculum and Semester 8 credit requirements remain unverified.
