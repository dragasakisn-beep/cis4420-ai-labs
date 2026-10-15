# CIS4420 | AI Security & Agent Development Laboratories

**Course:** CIS4420 — Secure Development Operations  
**Format:** Three guided, hands-on laboratory experiences  
**Focus:** AI security, large language models (LLMs), autonomous agents, and prompt injection  
**Framework alignment:** NIST SP 800-218 Secure Software Development Framework (SSDF); OWASP Top 10 for LLM Applications

## Course Objective

Develop foundational knowledge and practical skills for identifying, evaluating, and mitigating security risks in AI-enabled software systems. Apply secure development practices to LLM workflows, autonomous agents, and adversarial testing scenarios.

## Purpose and Intent

These exercises connect classroom instruction to practical AI security work. Students will explore how AI systems handle instructions and external information, identify misplaced trust and unsafe behaviors, and propose proportionate safeguards. The goal is not simply to make an AI system fail; it is to understand **why** a failure happens and how secure design can prevent or limit it.

## Launch the Interactive Lab Portal

Open **[CIS4420 Interactive Lab Portal](./index.html)** to view all three experiences in one page. If GitHub Pages is enabled, launch the portal from the repository's published Pages URL.

> **Instructor setup:** Name the supplied `CIS4420_Modern_Interactive_Labs.html` file `index.html` and place it in the repository root alongside this `README.md`. The relative link above works from the published website; in the GitHub file viewer, select `index.html` or open the Pages URL.

## Laboratory Overview

| Lab | Topic | Primary Skill | Launch |
| --- | --- | --- | --- |
| 01 | Huntr AI Security | Manual adversarial testing and trust-boundary analysis | [Open Huntr Challenges](https://huntr.com/challenges) |
| 02 | Hugging Face AI Agents | LLM and agent workflow fundamentals | [Open Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction) |
| 03 | Prompt Injection Labs | Injection analysis and defense recommendations | [Open PromptTrace Labs](https://prompttrace.airedlab.com/labs) |

---

## Lab 01 — Huntr AI Security: Adversarial Testing

**Course objective:** Recognize how LLM-based assistants may cross trust boundaries or mishandle instructions when exposed to adversarial content.

**Purpose:** Experience an authorized AI security challenge environment and observe how model behavior can diverge from intended security requirements.

**Intent:** Develop disciplined, ethical testing and evidence-based vulnerability analysis—not indiscriminate exploitation.

### Student Instructions

1. Open [Huntr AI Security Challenges](https://huntr.com/challenges).
2. Read the platform's **current rules of engagement** and select an available challenge. Sign in if the platform requires it.
3. Identify the assistant's intended task, protected information, and relevant trust boundaries.
4. Form a hypothesis about a possible failure mode (for example, treating untrusted material as authoritative instructions).
5. Conduct **manual, human-authored** tests only, within the challenge's permitted scope. Do **not** use bots, scripts, automated scanners, fuzzers, or other prohibited automation.
6. Record the test input, observed behavior, and why the result does or does not indicate a security weakness. Do not disclose challenge secrets or credentials in your submission.
7. Recommend at least two controls, such as instruction/data separation, least-privilege tool access, output filtering, or human approval for consequential actions.

**Student deliverable:** A brief test record showing one hypothesis, one or more authorized test attempts, observed outcomes, and two proposed mitigations.

**Completion criterion:** Explain a trust boundary, demonstrate an authorized test, and connect the observation to defensible security controls. A successful bypass is **not required**.

---

## Lab 02 — Hugging Face: LLMs and AI Agents

**Course objective:** Describe the components of an AI agent and assess risks created by tool use, context, and autonomous workflow execution.

**Purpose:** Build conceptual familiarity with LLM-based agents before evaluating their security architecture.

**Intent:** Shift students from thinking about AI as chat-only software to thinking about AI as a system that can interact with data, tools, and external services.

### Student Instructions

1. Open the [Hugging Face Agents Course — Unit 0](https://huggingface.co/learn/agents-course/en/unit0/introduction).
2. Complete the introductory material and proceed to the agent fundamentals content linked by the course, as accessible.
3. Define an **LLM**, an **agent**, a **tool**, an **observation**, and an **agent loop** in your own words.
4. Sketch an example workflow: **User request → model decision → tool call → external result → model response**.
5. Mark every point at which the agent accepts external input or requests permission to take an action.
6. Identify three realistic risks (for example, untrusted tool output, over-permissioned tools, or leakage of sensitive context).
7. Map each risk to a safeguard, such as input validation, tool allowlisting, scoped credentials, sandboxing, logging, or human approval.

**Student deliverable:** One agent workflow diagram, five concise definitions, and a three-row risk/control table.

**Completion criterion:** Correctly distinguish an agent from a chatbot and explain how security changes when an LLM can use tools.

---

## Lab 03 — Prompt Injection: Attacks and Defenses

**Course objective:** Differentiate legitimate user instructions from untrusted content and evaluate prompt-injection vulnerabilities and corresponding defenses.

**Purpose:** Examine how instructions embedded in untrusted material may attempt to redirect an AI system.

**Intent:** Practice systematic vulnerability analysis and defense-in-depth design in a controlled laboratory setting.

### Student Instructions

1. Open [PromptTrace Labs](https://prompttrace.airedlab.com/labs).
2. Review the site's current exercise instructions, prerequisites, and authorized scope.
3. Select an introductory prompt-injection scenario available on the platform.
4. Identify the **trusted instruction**, the **untrusted entry point**, the **attacker-desired deviation**, and the **potential security impact**.
5. Perform only the interactions authorized by the lab. Do not test unrelated systems or submit real credentials, personal information, or confidential documents.
6. Document the observed result and classify the attempted injection as **direct** or **indirect**, explaining your reasoning.
7. Propose at least two mitigations. Consider separating instructions from data, constraining tool privileges, validating outputs, and requiring approval for high-impact actions.
8. Reassess the scenario: describe what evidence would demonstrate that your proposed safeguards are effective.

**Student deliverable:** A short injection analysis identifying the entry point, trust boundary, observed behavior, likely impact, and two defenses.

**Completion criterion:** Accurately explain the injection mechanism and defend a realistic mitigation strategy. Successful exploitation is **not required**.

---

## Common Submission Requirements

Submit one combined report or three short lab records, as directed by the instructor. For **each** lab, include:

1. **Objective and scenario:** What were you attempting to learn or test?
2. **Procedure:** What steps did you perform, within the permitted scope?
3. **Evidence:** A concise observation, sanitized screenshot, or workflow diagram.
4. **Analysis:** What trust boundary, vulnerability, or design consideration did you identify?
5. **Mitigation:** What specific security controls would reduce the risk?
6. **Reflection:** How does the experience relate to secure development operations?

Do not include passwords, API keys, personal data, live challenge secrets, or other sensitive information in coursework.

## Rules of Engagement and Academic Integrity

- Work exclusively within each platform's explicitly authorized environment and follow its current rules.
- **Huntr prohibits automated attack tooling for its challenge environment:** tests must be human-authored and manual.
- Do not target third-party services, other students, or systems outside the exercise scope.
- Clearly distinguish **observed results** from **hypotheses** or **assumptions**.
- Cite any external material or tooling used, following course requirements.
- Platform availability, registration requirements, and challenge content may change; follow the live platform instructions when they differ from this guide.

## Expected Learning Outcomes

By the end of the three experiences, students should be able to:

- Explain the security implications of LLM and autonomous-agent architectures.
- Identify prompt-injection entry points and critical trust boundaries.
- Conduct and document permitted AI security testing.
- Recommend layered safeguards using least privilege, input/output controls, monitoring, and human oversight.
- Connect laboratory observations to secure software development practices and risk management.

---

**CIS4420 — Secure Development Operations**  
*Instructional lab guide · October 2026*
