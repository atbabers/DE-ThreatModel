# 4_risk_prioritization

<aside>

> **Warning**
> Detection Engineers should align their threat modeling efforts with their organization's risk management strategy, which may require adapting the formula to meet specific organizational needs, including the possibility of incorporating weights.
</aside>

## **4.1. Introduction to Risk Scoring Log Data**

We calculate risk using the formula:

$$
Risk=(L+D+A+P)×I
$$

<details>
  <summary><strong>Risk Prioritization Components</strong></summary>

  1. **Likelihood (L)**:
      - **Range**: 0-6
      - **Explanation**: This component measures the probability of the threat materializing in the context of your specific organization. A higher score means a greater likelihood of the threat occurring, while a score of zero suggests minimal or no chance.

  2. **Detection Difficulty (D)**:
      - **Range**: 0-7
      - **Explanation**: It gauges how challenging it is to detect a threat or suspicious activity in the environment. A higher score indicates a more complex detection process, while a score of zero denotes an easily detectable threat.

  3. **Asset Value (A)**:
      - **Range**: 0-10
      - **Explanation**: Represents the inherent value of the asset that is at risk. The asset could be infrastructure, data, or any other organizational resource. A higher score indicates a more valuable or critical asset.

  4. **Propagation Potential (P)**:
      - **Range**: 1-3
      - **Explanation**: This component assesses the potential of the threat to spread or propagate within the organization's environment. A score of 3 indicates a high likelihood of widespread propagation, while a score of 1 suggests limited spreading potential.

  5. **Impact (I)**:
      - **Range**: 1-3
      - **Explanation**: Directly related to "Threat Severity", this component evaluates the potential damage or consequences if the threat materializes. It accounts for both immediate and indirect implications, like data loss, system unavailability, reputational damage, or financial losses. A higher score indicates more severe potential repercussions.
</details>

**Maximum Score**

$$
Max Risk=(6+7+10+3)×3=78
$$

**Risk Categories and Their Ranges**:

| Risk Category | Score Range | Percentage of Maximum Score |
| --- | --- | --- |
| Low Risk | 0 - 19.5 | 0-25% |
| Medium Risk | 19.6 - 39 | 25.1-50% |
| High Risk | 39.1 - 58.5 | 50.1-75% |
| Critical Risk | 58.6 - 78 | 75.1-100% |

---

## **4.2. Risk Scoring Steps**

1. **Understand Log Data Value**: Recognize significance of logs.
2. **Assess Potential Damage**: Gauge harm from threats.
3. **Examine Existing Controls**: Identify protective measures and their impact on threat likelihood/impact.
4. **Calculate Likelihood & Impact**: Derive risk score.
5. **Prioritize Risks**: Address highest risks first, ranking by calculated Risk score.
6. **Continuous Review**: Update risk assessments regularly.