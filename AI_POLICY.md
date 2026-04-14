# AI Contribution Policy for the Strimzi Project

## Overview

Contributors may use AI tools, such as Large Language Models (LLMs) and code assistants, when contributing to Strimzi.
As with any development tool, the contributor is responsible for the quality of the result and for understanding what they submit.

**You are the contributor.** When you submit a Pull Request (PR) to Strimzi, you certify the contribution as your own work.
AI-generated or AI-assisted content does not change this responsibility.

## Requirements

### Understanding and Responsibility

* **You must understand your contribution.** Do not submit code, documentation, or other content that you do not fully understand. You should be able to explain to reviewers what your contribution does, how it works, and how you verified it.
* **Review all AI-generated content.** Before submitting, verify that the contribution is correct, tested, and follows the project's contributing guidelines.
* **Use AI as a learning tool.** New contributors could use AI tools to understand the codebase, patterns and best practices. If you're using AI to generate code you don't understand, take time to learn the concepts before submitting.
* **You own what you submit.** As the PR author, you are responsible for all changes, regardless of the tools used to create them.

### Disclosure

* **Disclose AI usage in your PR.** If AI tools play a significant role in a contribution, note this in the PR description.
* **Use the `Assisted-by` trailer.** Commits with substantial AI assistance SHOULD include an `Assisted-by` trailer identifying the tool and model used.
  
  Example commit message:
  ```
  Fix reconciliation loop for Kafka cluster scaling
  
  The operator was not properly updating the StrimziPodSet replica count
  when scaling Kafka clusters.
  
  Assisted-by: Claude Sonnet 4.5 <noreply@anthropic.com>
  ```
  
  You can add this trailer by using:
  ```sh
  git commit -m "Your commit message" --trailer "Assisted-by: <tool>/<model>"
  ```

  AI tools can be also configured to add this trailer automatically on commit.

* **When disclosure is required:** Disclosure is required when AI tools are used to generate substantial content. Using AI features similar to IDE capabilities does not require disclosure.
  
  **Examples of substantial assistance requiring disclosure:**
  - Generating entire methods, classes, or modules.
  - Creating entire test suites or documentation sections.
  - Refactoring significant portions of code.
  - Generating configuration files or build scripts.
  
  **Examples NOT requiring disclosure:**
  - Autocomplete suggestions (1-2 lines).
  - Syntax corrections and formatting.
  - Variable or method name suggestions
  - Spelling checks or grammar corrections.
  - Simple code completion similar to IDE features.

### What NOT to Do

* **Do not use AI tools as co-authors.** AI tools MUST NOT be added to `Signed-off-by` or `Co-authored-by` tags in commit messages. Only humans can legally certify the [Developer Certificate of Origin (DCO)](https://developercertificate.org/). The `Signed-off-by` tag certifies that you wrote the code or otherwise have the right to submit it under the project's license. An AI tool is not a legal entity and cannot make this certification.
* **Engage authentically with reviewers.** When maintainers, component owners or other contributors provide feedback on your PR, you may use AI tools to help craft responses, but you must fully understand and take ownership of what you write. Reviewers want to engage with you, not receive generic AI-generated replies. If you use AI assistance to formulate responses, ensure they genuinely reflect your understanding and that you can defend your reasoning.
* **Do not submit large AI-generated PRs.** AI tools can generate content faster than reviewers can read it. Keep PRs focused and appropriately sized. Strimzi maintainers MAY close pull requests that are too large to review effectively or where the contributor does not appear to understand the changes.
* **Avoid verbose AI-generated content.** Trim down unnecessary verbosity in PR descriptions, commit messages, and code comments. Be clear, concise, and specific. Respect the time of maintainers and reviewers.

### Quality Standards

* **Meet the same standards.** AI-assisted contributions are reviewed to the same standard as any other contribution. Code must be correct, maintainable, well-tested, and consistent with project conventions.
* **Ensure licensing compliance.** AI-generated content must not introduce material under licenses incompatible with the project's [Apache 2.0 License](./LICENSE).
* **Test your changes.** All code contributions must be tested according to the project's standards, whether AI-assisted or not.

## Consequences of Non-Compliance

Pull Requests that violate this policy may be closed. Specific cases include:

* PRs where the contributor cannot explain or defend the changes during review.
* PRs with generic, inauthentic responses to reviewer feedback that demonstrate a lack of understanding.
* Large, unfocused PRs that appear to be bulk AI-generated content.

## AI-Assisted Pull Request Reviews

Automated or AI-assisted reviews, can supplement the review process but do not replace review by maintainers or component owners.

* **AI reviews don't replace human review.** Automated checks and AI-generated review comments can provide useful signals (e.g., identifying security vulnerabilities, style issues, or potential bugs), but they do not satisfy the project's review requirements.
* **Humans make the decisions.** Maintainers and component owners make merge decisions following the project's [governance framework](./GOVERNANCE.md#pr-approval-rules). PR approval requires votes from maintainers and/or component owners as defined in the governance policy.
* **Contributors should engage with human reviewers.** While you may find AI-assisted review tools helpful during development, your PR must be reviewed and approved by project maintainers or component owners before merging.

## AI-Assisted Strimzi Proposals

[Strimzi proposals](https://github.com/strimzi/proposals) are strategic documents that significantly impact users or project direction. Due to their importance, special considerations apply:

* **AI-assisted proposals require deep understanding.** If you use AI tools to help draft a proposal, you must have a thorough understanding of the problem space, proposed solution, alternatives considered, and implications for users and the project.
* **The rationale matters most.** Proposals are not just about "what" to do, but "why" it should be done, what alternatives exist, and what trade-offs are being made. AI tools may help structure these thoughts, but the reasoning must come from genuine understanding of the project and its users.
* **Disclose AI usage.** If AI tools play a significant role in drafting a proposal, note this in the PR description.
* **Engage authentically in discussions.** Proposal discussions involve community consensus-building and voting. You must engage directly with the community, not through AI-generated responses. Maintainers and community members need to understand your reasoning and evaluate the proposal based on your understanding, not an AI's output.
* **AI-assisted reviews of proposals.** You may use AI tools to help you understand and evaluate proposals, but your vote or feedback must reflect your own judgment and reasoning.

Proposals that appear to be largely AI-generated without genuine understanding of the problem space MAY be closed by the maintainers.

## Questions

If you have questions about this policy or are unsure whether your use of AI tools requires disclosure, please contact the maintainers.
