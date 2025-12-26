\# DiagLogic  

Explainable diagnostic reasoning over vehicle diagnostic data  

(formerly OBD-AI)



---



\## What this is



DiagLogic is an engineering framework for vehicle diagnostics  

that structures human reasoning instead of making decisions for the user.



It is designed to work with:

\- OBD DTCs,

\- raw scanner logs,

\- multibrand diagnostic data.



DiagLogic transforms diagnostic data into a clear, explainable diagnostic plan,  

with explicit limits and honest acknowledgment of uncertainty.



---



\## What DiagLogic is NOT



DiagLogic is explicitly not:



\- a chat assistant  

\- an “AI that guesses the failure”  

\- a parts replacement recommendation system  

\- an automatic problem solver  



If you are looking for a tool that tells you “what to replace”,  

this project is not for you.



---



\## Who this project is for



DiagLogic is built for:



\- professional vehicle diagnosticians, not parts changers;

\- engineers who think in cause-and-effect logic;

\- practitioners who value explainability, safety, and reproducible diagnostics.



---



\## Core principle



A mechanical fault is a diagnosis of exclusion.



DiagLogic enforces this order by design:



1\. electrical plausibility  

2\. presence of a control command  

3\. presence or absence of system response  

4\. only then mechanical suspicion  



This order cannot be bypassed by the system.



---



\## How it works



OBD data, logs, and reports are processed through a deterministic pipeline:



Normalization  

Playbook selection  

Gated prioritization  

Structured diagnostic plan  

Explicit data gaps



The output is a report, not a conversation.



---



\## What a playbook means in DiagLogic



A playbook is formalized diagnostic logic, represented as data rather than code.



Each playbook defines:

\- problem context;

\- ordered checks;

\- confirmation conditions;

\- disconfirmation conditions;

\- explicit data gaps and their purpose;

\- safety constraints.



A playbook does not advise. It explains diagnostic reasoning.



---



\## Real-world value example



In a real diagnostic case involving:

\- P1117 (O2 heater short to ground),

\- P0402 (EGR excessive flow),



DiagLogic:

\- prevents immediate mechanical assumptions about the EGR valve;

\- forces consideration of an electrical root cause first;

\- stops exactly where data is insufficient;

\- clearly explains why further conclusions are not justified without logs.



This reduces false diagnoses, unnecessary disassembly, wasted time, and loss of trust.



---



\## Why there is no chat interface



Chat interfaces create an illusion of understanding, hide reasoning steps,  

and encourage premature conclusions.



DiagLogic follows a strict model:

analysis, explanation, re-evaluation.



Not conversation.



---



\## Project status



Current version: v0.1.1 (frozen)



The architecture has been validated on real-world cases  

across different vehicle platforms.



The project is multibrand by design  

and focused on explainable reasoning rather than automated decisions.



---



\## License



The license will be defined separately.



The project allows commercial use  

while protecting logic, safety, and its underlying philosophy.



---



\## In short



DiagLogic does not tell you what is broken.  

It shows you how to think correctly to avoid being wrong.

