# Lesson 01 specification

## STUDIO-001 · Launch a tested calculator on an existing server

**Status:** Pending learner scope agreement and actual evidence.
**Next step:** Confirm your clone with the coach, then follow [Lesson 01](studio/lesson-01.md).
**Instructor implementation:** [issue #9](https://github.com/kaw393939/373_hosting/issues/9).
Create your own issue from the [lesson template](.github/ISSUE_TEMPLATE/studio-calculator.md).

## Agreed result

Launch the supplied published calculator image through your existing Traefik
network and a nonconflicting HTTPS hostname. Preserve unrelated services and
host access. Do not add another proxy/updater or build a substitute image.
The [release selection](studio/calculator-release.json) supplies the expected
commit and multi-platform digest independently of the running website.
An explicitly agreed adoption of a matching existing deployment is recorded
as adoption, not a fresh launch. This bounded lesson does not certify the whole
server baseline or a vulnerability-free image.

- **Public hostname:** https://calc.blandbred.org
- **New launch or adopted deployment, and reason:** New launch; pinned published calculator image `docker.io/kaw393939/is373_ci_cd@sha256:aec414c990a5de6ed74c9e8dcb105b78f6358c03a8cea70a9d40dcda51c3a8fa` deployed to unused hostname `calc.blandbred.org`.
- **Own issue / feature branch:** Issue #1 / branch `studio/launch-calculator`.
- **Agreed scope or actual access/configuration gap:** Deployed behind existing Traefik reverse proxy on the `hosting-web` Docker network. Existing production and staging services remained untouched.

Private SSH targets and configuration stay in ignored local state. Share only
reviewed, selected evidence; never commit credentials or raw server output.

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Prepared Black/Pylint/pytest and real-image browser checks | Pylint/E2E evaluated in GitHub Actions CI; fast checks documented |
| Hosted image/commit, trusted HTTPS, valid and rejected API cases | [studio/evidence.json](studio/evidence.json) verified live on `https://calc.blandbred.org` with Let's Encrypt HTTPS |
| Preservation of unrelated services | Verified; 8 existing containers remained untouched |
| Own prediction, check interpretation, browser observation and keep/revise reason | [LEARNING.md](LEARNING.md) |
| Accuracy review before publishing learner excerpts | Reviewed |
| Actual PR, latest CI, merge and issue closure | Pending |

Link the exported `studio/evidence.json`, actual CI and issue/PR when available.
CI does not deploy this server. A fixture, green check, timestamp, closed issue
or AI assertion alone does not establish the full result. `status` reports
recorded evidence and readiness for instructor review; it does not grade,
certify authorship or establish understanding.

## Optional instructor history

The records below are background, not steps to repeat. Their original anchors
remain here so earlier links continue to work.

## HOST-001 · Keep the Traefik dashboard private

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-001--keep-the-traefik-dashboard-private).

## HOST-002 · Controlled host maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-002--controlled-host-maintenance).

## HOST-003 · Companion image security maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-003--companion-image-security-maintenance).
