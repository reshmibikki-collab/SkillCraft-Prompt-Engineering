**TASK 3: PROMPTING FOR TASK AUTOMATION**

**Objective:**

Automate health and fitness habit analysis by converting unstructured user statements into structured JSON data.



**1. Reusable Prompt:**

You are a health and fitness habit analyst. Your task is to analyze the given user statement and extract the required information.

Extract the following fields:

Activity 

Category 

Frequency 

Goal 

Action Required 

**Rules:**

Use only the information provided in the user statement. 

Do not invent or assume any missing information. 

If no specific activity is mentioned, return "None". 

Keep the output concise and clear. 

Category must be one of: "Exercise", "Nutrition", "Sleep", "Hydration", or "Other". 

Frequency should contain the frequency mentioned by the user. If no frequency is mentioned, return "None". 

Goal should contain the goal mentioned by the user. If no goal is mentioned, return "None". 

For Action Required, provide a concise action based only on the information provided. If no action is needed, return "None". 

Always return the result in the same JSON format. 

**Output format:**

{

&#x20; "Activity": "",

&#x20; "Category": "",

&#x20; "Frequency": "",

&#x20; "Goal": "",

&#x20; "Action Required": ""

}

User Statement:

\[Insert user statement here]



**2. Input-Output Examples:**

Example 1:

Input:

“I walk for 30 minutes every morning because I want to stay active and improve my fitness.”

Output:

{

&#x20; "Activity": "Walking for 30 minutes",

&#x20; "Category": "Exercise",

&#x20; "Frequency": "Every morning",

&#x20; "Goal": "Stay active and improve fitness",

&#x20; "Action Required": "Continue the daily walking routine"

}



Example 2:

Input:

“I drink more water during the day because I want to stay hydrated.”

Output:

{

&#x20; "Activity": "Drinking more water",

&#x20; "Category": "Hydration",

&#x20; "Frequency": "During the day",

&#x20; "Goal": "Stay hydrated",

&#x20; "Action Required": "Continue drinking water regularly"

}



Example 3:

Input:

“I usually sleep for seven hours every night.”

Output:

{

&#x20; "Activity": "Sleeping for seven hours",

&#x20; "Category": "Sleep",

&#x20; "Frequency": "Every night",

&#x20; "Goal": "None",

&#x20; "Action Required": "None"

}



**3. Reflection:**

Initially, my prompt did not specify fixed values for the category field or clearly define how missing information should be handled. This could produce inconsistent outputs. I improved the prompt by defining allowed values for the category, specifying "None" for missing information, and requiring a consistent JSON format. I tested the revised prompt with different health and fitness statements and found that the outputs became more structured, consistent, and reliable.



