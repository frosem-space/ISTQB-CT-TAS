<p align="center">
  <a href="https://istqb.org/certifications/certified-tester-test-automation-strategy-ct-tas/">
    <img src="https://istqb.org/wp-content/uploads/2024/10/CT_TAS-1024x940-1.png" width="200" alt="ISTQB CT-TAS Logo"/>
  </a>
</p>

# Chapter 5: Test Automation Impact Analysis

| K-Level | Code            | Learning Objective                                                                 | Number of Questions | Suggested Points |
|---------|------------------|-------------------------------------------------------------------------------------|---------------------|------------------|
| K3      | CT-TAS-5.1.1     | Show the return on investment of building a test automation solution                | 2                   | 2                |
| K2      | CT-TAS-5.2.1     | Classify metrics for test automation                                               | 1                   | 1                |
| K3      | CT-TAS-5.3.1     | Identify organizational considerations for the use of test automation               | 1                   | 2                |
| K3      | CT-TAS-5.3.2     | Analyze project characteristics to determine optimal test automation objectives     | 2                   | 2                |
| K2      | CT-TAS-5.4.1     | Analyze test report data to inform decision making                                  | 1                   | 1                |

**Total Questions: 7**  
K2 = 2  
K3 = 5  
**Total Points: 12**

---

## 5.1 Investment in Setting Up and Maintaining Test Automation

### 5.1.1 Show the Return on Investment (ROI) of Building a Test Automation Solution

To evaluate whether test automation is worth implementing, consider both the effort to build and maintain the automation and the benefits it provides.

**ROI Formula**:  `ROI = Savings / Investment`

**Savings** – Calculated based on:  
- Time saved running automated vs. manual tests.  
- Number of test cases and executions possible with automation.  
- Increased frequency of test execution.  

**Investment** – Calculated based on:  
- Time to set up the TAS  
- Development and maintenance time per script  
- Number of scripts  
- Time to run each script  
- Failures and retries  

To compare costs in a unified way, convert financial costs into time using hourly rates if necessary.

**Important Considerations**:  
- If ROI doesn’t turn positive within the project’s duration, it is not worth introducing test automation.
- Applying the **test pyramid** in the respective test levels can reduce runtime and increase ROI.
- Graphing sprints vs. ROI can help identify when benefits will start exceeding the investment.

---

## 5.2 Test Automation Metrics

### 5.2.1 Classify Metrics for Test Automation

Measuring TAS performance helps assess suitability, adaptability, and maintainability. Metrics should be easy to collect, ideally automated, and cost-effective.

| Metric                        | Purpose / Insight |
|------------------------------|-------------------|
| **Pass-fail ratio**           | Tracks passed vs. failed tests. Useful for trend analysis. |
| **Failures per defect**       | Highlights if one defect causes multiple test failures. Helps with root cause analysis. |
| **Execution time**            | Tracks total run time and build time. Becomes more important as test count grows. |
| **Number of automated tests** | Shows progress but does not reflect test coverage. |
| **Functional coverage**       | Shows which functional requirements are tested automatically. |
| **Code coverage**             | Tracks how much code is exercised by automated tests. Not always necessary to aim for 100%, but higher is generally better. |

These metrics should be tracked continuously and used to guide improvements to the TAS.

---

## 5.3 The Value of Test Automation on the Project and Organization Level

### 5.3.1 Identify Organizational Considerations for Use of Test Automation

Before implementing automation, assess the following at the organizational level:

| Factor                          | Consideration |
|----------------------------------|---------------|
| **Policies & practices**         | Check development workflows, documentation (e.g., SUT specs, code standards), and integration points for automation. |
| **Existing TAS projects**        | Review current automation efforts to avoid duplication and identify reusable components. |
| **Subject matter experts (SMEs)**| Leverage expert knowledge and lessons learned to avoid known pitfalls. |
| **Test environments**            | Understand available environments, usage, and ownership to prevent conflicts. |
| **Tools & licenses**             | Use already licensed tools if suitable to reduce costs and avoid unnecessary setup. |

Proper assessment leads to better integration and cost-effective planning for TAS rollout.

---

### 5.3.2 Analyze Project Characteristics That Help Determine Optimal Implementation of Test Automation Test Objectives

Several project aspects influence how test automation should be introduced:

| Characteristic       | Impact on Test Automation |
|----------------------|---------------------------|
| **Domain**           | Each domain (finance, health, tourism) has specific regulations and risks to consider. |
| **Platforms**        | Consider all platforms (web, mobile, etc.) and determine if tools can be reused across them. |
| **Programming language and technology stack**       | Align test code with development languages to improve collaboration and maintainability. |
| **Maturity of the project**         | Evaluate test case count, existing CI/CD, and timelines. Avoid building full TAS if the project ends soon. |
| **Stakeholder buy-in** | Present a plan with benefits and risks to secure stakeholder support. Show how testability and product quality will improve. |
| **Team knowledge and relevant experience**   | Assess tester skills and identify training needs through competency mapping. |
| **Budget/support**   | Ensure test objectives align with available budget and test management support. Prepare clear documentation to justify costs. |
| **Quality characteristics** | Test Types. These quality characteristics can then be used for evaluating the current TAS, or determining metrics that will be collected by the TAS. |

---

## 5.4 Decisions Made from Test Automation Reports

### 5.4.1 Analyze Test Report Data to Inform Decision Making

Test automation reports provide data to inform decisions across various stakeholder levels (technical, operational, strategic).

**Purpose of the Reports**:
- Help identify trends and perform **root cause analysis**

- Support **test maintenance** and **TAF enhancements**

- Drive **shift-left** (early testing) and **shift-right** (production feedback) approaches

- Suggest ways to **improve test coverage**

- Highlight **defect clusters** or unstable areas

- Provide input for **developer improvements**

- Suggest **SDLC process enhancements**

- Tailor the **content and format** of future reports to stakeholder needs

**Collaboration between TAEs and stakeholders** is critical for identifying gaps, defining improvements, and increasing TAS effectiveness.

---

## Summary

- ROI evaluation for test automation requires time, cost, and benefit analysis. Introduce TAS only if the return will occur during the project.
- Use metrics to assess TAS performance and guide decisions—focus on coverage, execution trends, and failure analysis.
- Understand organizational readiness: tools, processes, existing environments, and SME input matter.
- Tailor automation to each project’s domain, tech stack, maturity, and stakeholder engagement.
- Test automation reports must drive actionable decisions—from technical fixes to strategic improvements in the testing process.

---

> ✅ **Strategically planning TAS with accurate metrics and realistic ROI ensures long-term success and adoption across the organization.**

> ⚠️ **Skipping ROI evaluation, ignoring stakeholder alignment, or collecting irrelevant metrics can reduce automation effectiveness and stakeholder trust.**

---
