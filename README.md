# FoodLink AI
End hunger, achieve food security and improved nutrition, and promote sustainable agriculture.


***Problem — Who is affected, and what specifically breaks down for them today?***

This project supports **SDG 2: Zero Hunger by helping food-insecure students and nearby residents get clearer next steps while helping pantry staff turn messy requests and donation information into usable records. Since M1, the topic stayed focused on Zero Hunger, but the scope is narrowed from the broad goal of “ending hunger” to a specific local workflow: food help intake, resource matching, and donation triage, because a narrower problem can be easier` tested in a working prototype. In this example scenerio we follow Diego, a first-year SJSU student who works evenings, lives off campus, and sometimes skips meals because he does not know which food pantry or community food resource can help him today. The failure point is not that food resources do not exist; it is that information is scattered, pantry intake questions are hard to answer quickly, and dietary needs such as halal, vegetarian, allergies, or low-sodium meals can be missed during intake.

***AI Capability — Which lab capability addresses the failure point, and why does it fit?***

All three labs are compatible with our goal! With slight modification, Lab 1: Text Generation, Lab 2: Structured Data Extraction, and Lab 3: Visual Recognition are all usable for the Zero Hunger project. Lab 1 supports communication with the person asking for help. Lab 2 turns a messy food-help request into fields pantry staff can use. Lab 3 supports donation intake by analyzing a photo of a donated food item or pantry shelf.

***Workflow — What goes in, what does the AI do, what comes out, and who acts on the output? Include screenshots of output***

System name: FoodLink AI Intake and Donation Assistant

Structured workflow:
Student send request or donation photo -> Google Gemini processes generation by structured extraction + visual recognition -> food need record and donation assessment -> Language output -> pantry and basic needs staff review generation result  -> real-world action

| Steps | What happens |
|---|---|
| **1. Input** | A student or resident submits a food help message, or a volunteer uploads a photo of donated food. |
| **2. AI processing** | Lab 1 drafts a respectful reply in written language. Lab 2 extracts structured fields like urgency, dietary needs, transportation barriers, and recommended action. Lab 3 analyzes a donation photo for visible item type, condition, and whether a human should inspect it. |
| **3. Output** | The system produces a response, a pantry intake record, and a donation assessment. |
| **4. Real-world action** | A food pantry worker or basic needs staff member reviews the AI output, contacts the person, confirms availability, then routes them to food pickup, emergency support, or donation handling. |

***Failure Case — One specific failure, with a reference to the lab output that showed it is possible.***

Prompt used: The edge case prompt describes a mixed Spanish/English request from a household with a 78-year-old diabetic grandmother, no car, limited phone access, urgent food need, and a dented unlabeled can.

Output returned: After running the code cell above, leave the Lab 1 response and Lab 2 output visible here in the notebook.

One-sentence assessment: This is a close miss if Gemini flags urgent human review but gives only general food advice. It becomes a failure if it suggests eating the dented unlabeled can, ignores the diabetes issue, or fails to mark the case for human review.

***Oversight and Tradeoff — Where does human review sit, and what does the one change cost?***

FoodLink AI's use of human review is a non-negotiable requirement. It is needed for verifiation of resource availability, ensuring the safety of food that are received, and the overall inspection of the donations. Due to the high use of human review though trade offs begin to arise. The more manual review that is used causes a slower process of resolution for the donator or requestee. Although a slower process, safety will always be our number one priority.
