# 2_log_data_characterization

<aside>

> **Note**
> With caution, this is a great time to begin identifying what events we can filter out, as they hold no bearing on any conceivable security event. We can leverage the [**Event Maturity Matrix**](https://github.com/AppOmni-Labs/event-maturity-matrix/) to aid in this process.
</aside>

## **2.1. Understand Log Structure**

### **2.1.1 Review Log Documentation**

Before delving into logs, consult any documentation or specifications for the log source to gain insights into its intended structure and data points.

### **2.1.2 Sample Analysis**

Analyze a log sample to discern its format and structure, identifying patterns, recurring fields, and separators.

### **2.1.3 Classify Fields**

Catalog and categorize the log fields, such as timestamp, user ID, event type, and so on.

### **2.1.4 Determine Data Types**

Identify the data type (e.g., string, integer, timestamp) for each field to aid in establishing parsing rules and facilitating analysis.

### **2.1.5 Identify Typical Values**

Record typical values for frequently occurring fields to expedite the detection of future anomalies or outliers.

---

## **2.2. Identify Key Events**

### **2.2.1 Catalog Common Events**

Compile a list of events types, including authentication, configuration, and user activity, encompassing both routine operations and security-related incidents.

### **2.2.2 Prioritize by Impact**

Rate each event type by its potential security impact, such as assigning a higher rating to an administrator changing a user's password than to a failed login attempt.

### **2.2.3 Seek Expert Insights**

Engage with system administrators, application owners, or log source experts, as their insights can distinguish between routine events and potential security concerns.

### **2.2.4 Catalog Essential Events**

Construct a catalog of essential events based on previously identified key occurrences, furnishing a deep comprehension of security threats and underscoring the necessity of consistent monitoring and in-depth analysis.