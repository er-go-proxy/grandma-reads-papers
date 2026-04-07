# Search Playbook

Use this playbook when the user provides only partial paper information or when related literature and code must be found.

## Paper Identification

If the user gives only a rough name or description:

1. Search the exact phrase plus likely domain keywords.
2. Prefer arXiv, publisher pages, or official project pages.
3. Confirm author names, year, and title before analyzing.

## Related Work Selection

Do not compare against a random list of vaguely similar papers.

Pick:

1. the direct baseline named by the paper
2. the classic paper that established the main paradigm
3. the closest competing alternative if it clarifies the novelty

For each related paper, extract only what is needed to explain the target paper:

- what problem it solved
- how it solved it
- what assumption it relied on
- what limitation opened the door for the new paper

## Code Search

Search in this order:

1. official repository linked from the paper or project page
2. official organization or first-author repository
3. well-known community implementation, clearly labeled as unofficial

When reading code, prioritize:

1. README and setup instructions
2. config files
3. model definition files
4. training loop and loss computation
5. evaluation or inference entry points

## Evidence Hierarchy

Trust order:

1. paper text and appendix
2. official code
3. official project page
4. third-party implementation
5. blog posts and forum explanations

Use lower-tier sources only to clarify, not to overwrite primary evidence.

## Comparison Checklist

When answering `what is actually new here?`, check:

1. changed architecture
2. changed objective or loss
3. changed data processing
4. changed training schedule
5. changed inference rule
6. changed benchmark setup
7. pure renaming or packaging

If the novelty mainly sits in evaluation, framing, or integration rather than the model core, say that explicitly.
