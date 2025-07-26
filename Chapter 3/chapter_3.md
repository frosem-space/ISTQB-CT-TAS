<p align="center">
  <a href="https://istqb.org/certifications/certified-tester-test-automation-strategy-ct-tas/">
    <img src="https://istqb.org/wp-content/uploads/2024/10/CT_TAS-1024x940-1.png" width="200" alt="ISTQB CT-TAS Logo"/>
  </a>
</p>

# Chapter 3: Preparing for Test Automation

| K-Level | Code            | Learning Objective                                                                                   | Number of Questions | Suggested Points |
|---------|------------------|-------------------------------------------------------------------------------------------------------|---------------------|------------------|
| K2      | CT-TAS-3.1.1     | Differentiate between test automation distributions                                                   | 1                   | 1                |
| K2      | CT-TAS-3.1.2     | Select a test automation approach based on the system under test architecture                        | 1                   | 1                |
| K3      | CT-TAS-3.1.3     | Demonstrate ways to optimize test automation distribution to achieve shift left and shift right       | 1                   | 2                |
| K2      | CT-TAS-3.2.1     | Explain how test automation projects conform with legacy software development lifecycle models        | 1                   | 1                |
| K2      | CT-TAS-3.2.2     | Explain how test automation projects conform with Agile software development best practices           | 1                   | 1                |
| K3      | CT-TAS-3.2.3     | Prepare for test automation projects to conform with DevOps best practices for continuous testing     | 1                   | 2                |
| K2      | CT-TAS-3.3.1     | Explain criteria for determining the suitability of tests for test automation                        | 1                   | 1                |
| K2      | CT-TAS-3.3.2     | Identify challenges that only test automation can address                                             | 1                   | 1                |
| K2      | CT-TAS-3.3.3     | Identify test conditions that are difficult to automate                                               | 1                   | 1                |

**Total Questions: 9**  
K2 = 7  
K3 = 2  
**Total Points: 11**

---

## 3.1 Integration Across Test Levels

### 3.1.1 Differentiate Between Test Automation Distributions

Different test distributions visualize how test types are spread across test levels. The ideal is the **pyramid**, but other shapes appear depending on system constraints, architecture, and automation maturity.

| Distribution      | Description |
|------------------|-------------|
| **Pyramid**       | Tests are concentrated at lower levels (component and service/API). Offers fast, stable tests. Preferred when time and resources allow. |
| **Ice Cream Cone**| Heavy UI-level testing with minimal component coverage. Costly and slower defect detection. Often due to lack of automation at lower levels. |
| **Hourglass**     | Component and UI test levels are emphasized, but service/API testing is weak. Increases integration risk. Common when business logic is spread. |
| **Umbrella**      | Nearly all testing happens at the UI level. Maintenance is expensive. A fallback when lower levels are technically untestable. |

The goal is to move from inefficient shapes (umbrella, ice cream cone) toward balanced pyramids by adjusting coverage and improving automation capability at each level.

---

### 3.1.2 Select a Test Automation Approach Based on the System Under Test Architecture

The SUT architecture defines what levels and types of automation are achievable.

- **Mainframe systems** often lack lower-level APIs and rely on terminal emulation. Automation focuses on UI, batch jobs, and database validations. Component testing is limited.

- **Microservices-based systems** allow component, API, and contract testing. These support more flexible and distributed automation.

In some cases, it’s not possible to apply lower-level automation, so the test strategy should set a realistic and progressive target distribution shape (e.g., moving from umbrella to hourglass, then to pyramid).

---

### 3.1.3 Demonstrate Ways to Optimize Test Automation Distribution to Achieve Shift Left and Shift Right Approaches

Improving test distribution requires a roadmap and priorities based on current vs. target state.

#### Shift Left

Focuses on earlier test execution in the development cycle:

- Introduce **component testing** early, especially if code coverage is low.

- Use **test doubles** (mocks, stubs) to reduce dependence on live systems.

- Apply **TDD**, reviews, and workshops to improve test quality.

#### Shift Right

Involves testing in pre-production or production environments:

- Use **canary releases** and **dark launches**.

- Monitor **real user interactions** and **API performance**.

- Combine automation with observability to support fast rollback decisions.

Shift left improves speed and stability. Shift right enhances user feedback and defect discovery in live conditions. Contract testing helps both shifts by reducing reliance on full end-to-end UI/API validations.

---

## 3.2 Strategic Considerations in Different Software Development Lifecycle Models

### 3.2.1 Explain How Test Automation Projects Conform with Legacy Software Development Lifecycle Models

- **Waterfall**: Testing happens late. Automation starts after design and coding. Feedback from automation comes too late to provide ROI.

- **V-model**: Test planning occurs earlier, but execution and TAS setup still come late. Slightly better ROI than waterfall but lacks flexibility.

These models reduce the impact of automation because the feedback cycle is too slow.

---

### 3.2.2 Explain How Test Automation Projects Conform with Agile Software Development Best Practices

- **Goal**: Achieve **in-sprint automation** where automation activities are completed within the same sprint as feature development.

- This includes defining, implementing, and integrating test cases as part of the user story's exit criteria.

- Less mature teams may need a buffer (1 sprint delay), then progress toward in-sprint automation.

- Test efforts must be estimated and tracked like development tasks.

Automation must be embedded into the sprint process, not treated as an afterthought.

---

### 3.2.3 Prepare for Test Automation Projects to Conform with DevOps Best Practices for Continuous Testing

DevOps supports **end-to-end automation** of build, integration, testing, deployment, and monitoring.

- Prioritize **low-level tests** (component, integration, contract) that run quickly and early.

- Integrate test execution into pipelines after local changes, pull requests, and deployments.

- Run heavier UI/API test suites as separate stages.

- Manual testing shifts to **exploratory** and **user experience validation**.

The goal is to provide continuous feedback with minimal human intervention and maximize automation coverage in each pipeline phase.

---

## 3.3 Applicability and Viability of Test Automation

### 3.3.1 Explain Criteria for Determining the Suitability of Tests for Test Automation

A test case is suitable for automation if:

- It is technically feasible to automate and maintain.

- The implementation effort provides enough ROI.

- The test needs to be run frequently.

- It belongs to critical suites like smoke, regression, or confirmation.

- It is stable, repeatable, and covers high-usage business workflows.

- There is reusability in steps or data.

- The team has the skills and tools to implement it.

### 3.3.2 Identify Challenges that Only Test Automation Can Address

Test automation is the only viable option when:

1. Execution time for manual testing is excessive.

2. Tests must run in parallel or be synchronized.

3. Results are required in CI/CD pipelines.

4. Logs or data must be parsed in large quantities.

5. Exact timing and delays matter.

6. The same test needs to be executed across multiple platforms or configurations.

7. Stress or reliability testing at scale is needed.

Automation supports consistency, coverage, and speed that are not possible manually.

---

### 3.3.3 Identify Test Conditions that are Difficult to Automate

Not all tests are automatable. Some examples:

- **Design validation** or UI consistency across devices, where human judgment is required.

- **Human-in-the-loop processes**, such as financial approvals, where business rules are applied manually.

- **OS-level restrictions**, such as mobile OS notifications or native prompts not exposed to automation tools.

- **Time-dependent tests** that require waiting (e.g., session timeout after hours) and cannot be sped up or mocked.

Such cases should be handled manually or through hybrid strategies.

---

## Summary

- Test automation distribution should move toward a pyramid, adapted to system architecture and test level access.
- Legacy models reduce automation ROI. Agile and DevOps support fast feedback and in-sprint or pipeline-level automation.
- Test automation is essential when speed, precision, scale, or repeatability is required.
- Some conditions still need manual handling due to technical, timing, or judgment constraints.

---
> ✅ **Design your automation distribution around what is achievable now and evolve it based on feedback and architecture.**
---
> ⚠️ **Avoid relying heavily on UI automation or manual testing when better options exist at lower test levels.**
---
