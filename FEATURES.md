# Features and specification

## Context
An intern placed on one team becomes curious about another team and wants firsthand information before deciding whether to pursue a formal move. The system helps the intern make a low-stakes connection and request an informational conversation or informal shadowing opportunity, so the intern can test whether the work is a genuine fit without prematurely signaling dissatisfaction or requesting a transfer.

## Users
Profiles and evidence in USERS.md: Primary users are interns fitting PROFILE-01 (The Hesitant Explorer), who have not yet reached out to anyone on the team they are curious about, and PROFILE-02 (The Proactive Outreacher), who represents the outcome the system should make repeatable. He proves that reaching a receptive contact without an existing personal connection works.

## Scope
This specification covers a way for an intern to request and complete one short, informal, no-commitment conversation with someone from a different team. The request is visible to the intern's current manager, framed as standard program participation rather than a signal of dissatisfaction, and carries an explicit guarantee of no negative impact on the intern's standing.

This specification does not cover: a formal internal transfer or rotation application process; matching guarantees or scheduling automation beyond a single request/response; performance or full-time-offer decisions; or support for full-time employees exploring outside teams (interns only).

### Kano hypotheses
Provide at least six features. For each, name the user segment, date, category, and evidence-based reasoning. These are tentative hypotheses, not validated survey findings.

| Feature ID | Feature | Kano hypothesis | Segment / date | Evidence and reasoning |
|---|---|---|---|---|
| F-01 |Opt-in directory of employees willing to have a 15-20 minute informal conversation with an intern from another team.  |Must-be |Both segments - Sept 08 |INT-02 succeeded through cold outreach to first-year analysts he had no prior connection to, but he had to find those contacts himself with no help; INT-01 confirmed no formal process exists today to identify who is approachable. The gap is not the willingness on the receiving end, it is that nothing tells an intern who to reach out to first. |
| F-02 |Explicit "Information only/no commitment" framing on every conversation request |Performance |Hesitant Explorer - Sept 08 |INT-01 observed that framing a request as "can you tell me what your team does" carried meaningfully less perceived risk. More explicit non-commitment framing should track with more interns being willing to make the first ask. |
| F-03 |Current manager notified when a cross-team conversation happens, framed as standard program participation with an explicit no-standing-imapct gurantee |Performance |Hesitant Explorer - Sept 08 |INT-02 reported his manager's actual reaction was "pretty positive," and that talking his team earlier would have earned him support. This directly challenges the assumption that the current team would judge the intern for wanting to explore other teams. |
| F-04 |Static content pages of typical work per line of business |Indifferent |Both segments - Sept 08 |This already exists informally through conversations and google. INT-02 shows firsthand, shadowing is what actually confirmed his interest. More content is unlikely to move the outcome. |
| F-05 |Formal application required just to start an exploratory conversation |Reverse |Both segments - Sept 08 |Both interviews show the value came from low-commitment, informal contact. Requiring paperwork to even start exploring would reintroduce the friction and exposure both segments are trying to avoid,  discouraging the exact behavior it claims to enable. |
| F-06 |Anonymized visibility into how many interns have completed exploratory conversations |Attractive |Both segments - Sept 08 |Neither interviewee asked for this, but it directly targets the perceived vs actual risk gap both interviews surfaced. Giving interns social proof that exploration is common and safe would make them more comfortable. |


## Behavior
1. When an intern views the directory, the system shall show only employees who have actively opted in as available for an informal conversation.
2. When an intern submits a conversation request to a listed employee, the system shall label the request as informational and non-committal in the message the employee receives.
3. When an intern submits a conversation request, the system shall notify the intern's current manager that the request was made, framed as standard program participation rather than a signal of dissatisfaction.
4. When an employee accepts a request, the system shall provide both parties a way to schedule a time within 5 business days.
5. If an employee does not respond to a request within 3 business days, then the system shall notify the intern that the request has gone unanswered and allow them to select a different employee.
6. While an intern's internship is active, the system shall allow that intern to submit requests to more than one line of business.
7. If an intern's internship end date passes, then the system shall disable that intern's ability to submit new requests.

## Constraints
- Only current employees and interns of the organization may access the directory; the system must sit behind existing internal authentication.
- An employee's opt-in status must be self-managed and revocable at any time.
- The organization must commit that a cross-team conversation request carries no negative weight in an intern's performance review or return-offer decision; this guarantee must be visible to the intern before they submit a request.
- The organization must make it clear to the intern and team that this is not a formal request for transfer.
- The system must retain no conversation content, only the fact that a request was made and its status.

## Acceptance
- WHEN an intern requests a conversation, THE SYSTEM SHALL confirm submission within 2 seconds.
- WHEN an intern completes two cross-team conversations in a single internship, THE SYSTEM SHALL show that intern's current manager was notified of both and THE SYSTEM SHALL show no negative flag recorded against that intern as a result.
- WHEN an employee opts out of the directory, THE SYSTEM SHALL remove them from intern-visible search results within 1 minute.
- WHEN an internship end date is reached, THE SYSTEM SHALL disable request submission for that intern by the next calendar day.
- WHEN completing an exploratory request, THE SYSTEM SHALL NOT create or submit a transfer request.


## Handoff reflection
A competent stranger picking this up would still need to ask: who decides which employees are eligible to opt in as volunteers (any employee, or only those in good standing with their own manager?), what happens if an intern requests more conversations than the volunteer pool can support, whether this should extend beyond corporate banking to the rest of the organization or stay pilot-scoped to one division first, and — since the design now makes requests visible to the current manager instead of hiding them — what actually enforces the no-standing-impact guarantee, since a policy that's easy to state is not automatically a policy that's easy to trust.

## AI assistance
I used AI to make sure I met all the requirements by running my entry through Copilot and having it compare my assignment to the rubric.
