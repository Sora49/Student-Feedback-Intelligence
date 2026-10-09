# Student Feedback Intelligence
### Group 5 — NLP-Based Analysis of Student Feedback

**Roll Numbers:** J025, J026, J027, J028, J030

## 1. Overview

Universities collect large volumes of textual feedback through course evaluations, student surveys, and online learning platforms. Numerical ratings provide a useful overview, but they often fail to explain *why* students liked or disliked a course or what could be improved.

**Student Feedback Intelligence** is a proposed Natural Language Processing (NLP) system that analyses open-ended student feedback, identifies the aspects being discussed, determines the sentiment associated with each aspect, discovers recurring topics, and produces concise, actionable reports for educators and administrators.

## 2. Problem Statement

Faculty and university administrators may struggle to review large amounts of student comments manually. Aggregate ratings alone do not always reveal specific strengths and concerns, such as teaching quality, lecture pace, assignment difficulty, or workload.

The proposed system aims to transform unstructured feedback into structured insights that can support evidence-informed improvements in teaching and learning.

## 3. Intended Users

- **Faculty and instructors:** Identify course strengths and areas for improvement.
- **Course coordinators:** Compare recurring issues across courses and semesters.
- **Department heads:** Recognise department-level patterns.
- **Quality-assurance teams:** Monitor teaching and learning trends.

## 4. Input Data

The system may analyse text collected from:

- Course evaluation forms
- Student surveys
- Open-ended feedback questions
- Online learning platforms
- Course and instructor review forms

## 5. Expected Outputs

For example, consider the feedback:

> “The lectures were very informative, but the pace was too fast and the assignments were difficult.”

The system could identify the following aspects and sentiments:

| Aspect | Sentiment |
|---|---|
| Lectures | Positive |
| Lecture pace | Negative |
| Assignments | Negative |

A feedback report may also include:

- **Top positive aspects:** Teaching quality, informative lectures
- **Top concerns:** Lecture pace, assignment difficulty, workload
- **Representative keywords and phrases**
- **Recurring topics and clusters of similar comments**
- **Sentiment distributions**
- **Changes in feedback over time**, where historical data is available

These outputs are intended to summarise patterns in the feedback rather than replace human judgement.

## 6. NLP Tasks

### Sentiment Analysis
Classifies feedback as positive, negative, or neutral.

### Aspect-Based Sentiment Analysis (ABSA)
Associates sentiment with specific aspects, such as lectures, pace, assignments, workload, and teaching quality.

### Topic Modelling
Discovers recurring themes across a large collection of feedback.

### Clustering
Groups similar comments to identify common concerns and patterns, including themes that were not predefined.

### Keyword Extraction
Identifies important words and phrases associated with comments or topics.

### Summarisation
Converts large volumes of feedback into concise summaries of key strengths and concerns.

## 7. Dataset

The proposed primary dataset consists of approximately **6,500 stratified samples of English-language public tertiary student review texts**, released between **2020 and 2023**. The project proposal describes the reviews as covering courses, teaching staff, and universities, and attributes the collection to the University of Liverpool and the University of Exeter.

**Dataset verification note:** Confirm the dataset's official title, source URL, licensing conditions, sample count, and institutional attribution before implementation. These details should be documented here once verified.

## 8. Proposed Approach and Architecture

The initial workflow is:

1. **Preprocessing:** Clean the text, normalise formatting, and remove personally identifiable information where present.
2. **Sentiment classification:** Classify feedback or relevant text segments as positive, negative, or neutral.
3. **Aspect extraction:** Identify the course or teaching aspects discussed in each comment.
4. **Topic modelling and clustering:** Discover recurring themes and group similar feedback.
5. **Keyword extraction:** Identify terms and phrases that help describe each theme.
6. **Summarisation:** Generate concise summaries of major strengths and concerns.
7. **Reporting and dashboard:** Present findings by course, semester, department, or instructor, subject to data availability and appropriate privacy safeguards.

## 9. Evaluation

The system will be evaluated using measures appropriate to each task:

- **Sentiment classification:** Accuracy, precision, recall, and F1-score.
- **Aspect extraction:** Precision, recall, and F1-score.
- **Topic modelling:** Topic coherence and qualitative review of topic interpretability.
- **Clustering:** Suitable clustering metrics and/or human evaluation.
- **Summarisation:** Human assessment of factual accuracy, coverage, and usefulness.
- **Error analysis:** Qualitative examination of false or misleading aspect–sentiment associations.

Evaluation should use suitable labelled data where available and clearly document the limitations of each metric.

## 10. Expected Institutional Value

Student Feedback Intelligence aims to turn large volumes of open-ended comments into clear, actionable insights. Rather than relying only on numerical ratings, educators and administrators could identify specific strengths and concerns—such as teaching quality, lecture pace, assignment difficulty, and workload—and use these patterns to guide course review and improvement.

The system is intended as a decision-support tool. Findings should be interpreted in context and reviewed by institutional stakeholders before decisions are made.

## 11. Privacy and Responsible Use

- Remove or mask personally identifiable information where present.
- Restrict access to raw comments and sensitive reports.
- Avoid presenting small groups of comments in ways that could identify individual students.
- Review model outputs for bias, errors, and misleading interpretations.
- Use aggregate findings responsibly and retain human oversight over institutional decisions.