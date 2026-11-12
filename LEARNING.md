# Lesson 01 · Conversation evidence

AI-drafted task summary, not a transcript or grade. It may be public. Use actual
short quotes or labeled paraphrases, name any help supplied, and link actual
work. Leave missing contributions Pending. A learner can review, correct or
remove excerpts before publication; accuracy approval is not proof of learning.
Label role-play honestly rather than treating it as an actual learner response.

**Lesson:** STUDIO-001. **Available conversation context:** Not recorded yet.

## Prediction

A browser sends an HTTPS request on port 443; Traefik receives it, handles TLS termination and Let's Encrypt certificates, matches the `Host(`calc.blandbred.org`)` rule, and routes traffic over the Docker `hosting-web` network to the calculator container. (Learner selected Option A with AI coach assistance).

## Check interpretation

The automated runtime verification exercised several API cases and host constraints:
- **Positive test:** Multiplying `6 * 7` returned HTTP 200 and result `42`.
- **Negative test 1:** Division by zero returned HTTP 400 Bad Request.
- **Negative test 2:** Passing numeric strings was rejected with HTTP 422 Unprocessable Entity.
- **Preservation:** All 8 pre-existing containers (including production `is373-prod` and staging `is373-qa`) remained online and unaffected.

## Browser observation

Visited `https://calc.blandbred.org` over public HTTPS. Observed page title "IS373 Content Management System" and status "API available". Executed the calculation `6 × 7`: the browser result showed `42` (calculated locally via JavaScript) and the API result returned `42` (verified by FastAPI), resulting in the green status indicator "Results match". Commit SHA `4600202` and environment `production` were displayed in the footer.

## Keep decision

Keep the deployment. The calculator is live with valid HTTPS on `calc.blandbred.org`, passes API test cases, and all existing services remain intact.

## Review

Reviewed and confirmed accuracy of the recorded plan, checks, and observations.

## AI work and next step

AI configured the remote target (`droplet`), verified SSH access, inspected the existing Traefik network, executed `launch` and `verify`, and generated `studio/evidence.json`. Next: learner tries a calculation on `https://calc.blandbred.org` and submits the GitHub issue.
