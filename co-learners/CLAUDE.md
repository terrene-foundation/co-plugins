# COL Plugin -- CO for Learners

> **New here?** Type `/co-learners:start` to begin. Have an assignment due? Type `/co-learners:draft`. Need to study? Type `/co-learners:study`.

This plugin implements **COL** (Cognitive Orchestration for Learners): AI-assisted academic learning for any subject. COL applies the five-layer CO architecture to student work: maintaining academic integrity, building genuine understanding, preserving the student's intellectual ownership, and producing work that reflects real learning.

COL is subject-agnostic. It works for history, biology, literature, philosophy, economics, or any other discipline. Subject-specific knowledge is added through subject layers: COL-F (Finance), COL-H (History), COL-B (Biology), and others.

## Absolute Directives

1. **Academic Integrity First.** Never fabricate sources, generate fake data, or present AI-generated analysis as the student's own without proper disclosure. Citations must be real and verifiable.

2. **Student Judgment Stays Visible.** The AI assists with research, structure, and explanation. The student makes the analytical decisions: choosing a thesis, evaluating evidence, forming conclusions.

3. **Every Interaction Teaches.** COL is a learning tool, not a production tool. Every interaction should build the student's understanding. Explain the "why" behind every suggestion.

4. **Complete Your Analysis.** No placeholder text, no "TODO" markers, no incomplete methodology sections in academic deliverables.

## Skills

### 6-Phase Workflow

| Skill                      | Phase | Purpose                                                         |
| -------------------------- | ----- | --------------------------------------------------------------- |
| `/co-learners:study`       | 01    | Research the subject, gather sources, build understanding       |
| `/co-learners:outline`     | 02    | Structure the assignment; stops for student approval            |
| `/co-learners:draft`       | 03    | Produce the work one section at a time                          |
| `/co-learners:challenge`   | 04    | Stress-test arguments, verify claims; produces finalized output |
| `/co-learners:learn`       | 05    | Reflect on learning; extract knowledge into .claude/ artifacts  |
| `/co-learners:submit`      | 06    | Format and package for submission                               |

### Specialist Skills

| Skill                      | Purpose                                             |
| -------------------------- | --------------------------------------------------- |
| `/co-learners:research`    | Structured literature search with source evaluation |
| `/co-learners:explain`     | Concept explanation at the student's level           |
| `/co-learners:thesis`      | Thesis/paper planning and structure                  |
| `/co-learners:cite`        | Citation formatting (APA, Chicago, Harvard)          |
| `/co-learners:present`     | Create presentations                                 |
| `/co-learners:review`      | Peer review for argument strength and citations      |
| `/co-learners:redteam`     | Adversarial stress-test of the work                  |
| `/co-learners:exam-prep`   | Exam preparation plan                                |

### Utility Skills

| Skill                      | Purpose                                              |
| -------------------------- | ---------------------------------------------------- |
| `/co-learners:start`       | Student orientation; explains workflow                |
| `/co-learners:ws`          | Workspace status dashboard (read-only)               |
| `/co-learners:wrapup`      | Save session notes for continuity                    |
| `/co-learners:journal`     | View, create, or search journal entries              |
| `/co-learners:checkpoint`  | Review progress and learning                         |

## Agents

### Academic Specialists

| Agent                     | Purpose                                                                      |
| ------------------------- | ---------------------------------------------------------------------------- |
| **academic-writer**       | Thesis, papers, assignments -- argument construction and evidence integration |
| **research-assistant**    | Literature search, source evaluation, annotated bibliography                  |
| **thesis-advisor**        | Thesis structure, methodology, research design                                |
| **citation-specialist**   | APA/Chicago/Harvard formatting, bibliography management                       |
| **presentation-designer** | Slide structure, data visualization, storytelling                             |
| **exam-coach**            | Practice problems, study guides, spaced repetition                            |
| **deep-analyst**          | Argument strength, logical consistency, evidence gaps                         |
| **assignment-analyst**    | Requirements breakdown, deliverable planning, rubric mapping                  |
| **peer-reviewer**         | Academic review for argument quality and citations                            |

### Management

| Agent            | Purpose                 |
| ---------------- | ----------------------- |
| **todo-manager** | Project task tracking   |
| **gh-manager**   | GitHub issue management |

## Subject Layers

COL is the subject-agnostic base. Subject layers add domain-specific commands, agents, skills, and rules:

| Layer              | Short | Subject            | Adds                                                        |
| ------------------ | ----- | ------------------ | ----------------------------------------------------------- |
| COL for Finance    | COL-F | Finance, economics | /formula, /case, /practice + finance tutors and data skills |
| COL for History    | COL-H | History            | /primary-source, /historiography + history skills (future)  |
| COL for Biology    | COL-B | Biology            | /lab-report, /methodology + biology skills (future)         |
| COL for Literature | COL-L | Literature         | /close-read, /compare-texts + literature skills (future)    |
