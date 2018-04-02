# Engineering Planning 4/2/2018

## Moderator / Notetaker: Yondon Fu
**Last Week**
- **Emphasis is on stability fixes and documentation**
- Decision and set up around ETH node used for distribution. Related to this is handling any connection breakage (Yondon)
- Make sure we are set up to handle any halting during the distribution and that we can recover (Yondon)
- Continue to formalize deployment and genesis checklist (Yondon)
- Work on fixing verification-computation-solver (Yondon, Eric)
  - Potential additional changes needed here related to latest transcoder changes for LPMS
- Test the revocation of the vesting contract (Eric)
  - Revocation of tokens not actually observed because revocation is only for unvested tokens and all the tokens has already vested by the time of revocation - will make a note to check again next time before all the tokens become vested
- Multisig key management decisions (Doug)
- Set protocol parameters (Doug)
- Set up a mainnet synced archive node (Eric)
  - Not done last week, but set up should be fairly straightforward and will be done this week
- Revisit devenv to get it up to date, update the developer doc along the way. (Eric)
- Update ReadTheDocs in support of launch (Doug to coordinate, but might need some team input)
  - A lot of helpful content has been created in other sources such as the forum, but ReadTheDocs still needs updating
- Add call reward functionality in the CLI
- Investigate transcoder behavior under load (Josh)
  - Didn’t get to actual simulations, but looked at the test suite with the goal of making sure the test suite is set up correctly to check this behavior
  - Eric has found some success with a local set up for testing that handles multiple transcoders - will try to document his process (Eric)
- AWS Infra review (Josiah and Eric)
  - Migrated to new prod environment after getting through some migration issues which will be described in a postmortem
- Participation UI/API testing and updates (Josiah)
- Synced with Raffi about analytics (Josiah)
- LivepeerJS housekeeping - updated docs, published latest packages to npm (Josiah)
- Attempted to merge basicnet; blocked on go-ipfs. Need to sync all gx deps. (Josh)
  - Will need better solution for upgrades in the future for maintainability

**This Week**
- Testing for new bitexact verification code in devenv and hoping to make the setup for that component in devenv easier (Yondon)
  - We should make sure that the versions used in the releases are exactly the same both in go-livepeer and the relevant verification code
- Simulate an airdrop distribution with thousands of recipients (Yondon)
- Review some of the progress made on the Truebit PoC on the Truebit side (Yondon)
- Mainnet deployment prep
  - Set up a full ETH node to sync with mainnet (Eric)
  - Documentation of tasks such as upgrades, revocation of vesting tokens, releasing vesting tokens, etc. (Yondon)
- Review new deployment procedures for AWS services (Eric + Josiah)
- Setup Google Analytics for livepeer.tv (Chris + Josiah)
  - Chris is owner so sync with him to figure this out
- LivepeerJS (Josiah)
  - CI Testing + coverage
  - Pre-commit hooks (linting / testing)
  - Looking to spend a little time each week to keep things up to date instead of doing giant batch updates in the future
- Continue updates for participation UI/API (Josiah)
  - Waiting on some clarification for potential copy and requirement info changes
- If registartion with participation app launches this week the #1 priority will be to address and support user experience in real time (Everyone)
- Explorer enhancements (Josiah)
  - Fix bugs, improve navigation, in-app tips
  - Plan updates on pre-launch timeline
  - There is a good chance that there will not be time for all of this week
  - Generally, this is high priority, but attempting to unblock other people as we get the partipation related stuff out the door this week
- Documentation for AWS infra updates (Eric)
- Broadcasting bug: same node different IP - cannot broadcast from home on my laptop (Eric)
- Ingest1 bug: node needed restart on Saturday.  Why? (Eric)
- End-to-end testing: change verification rate to 1/100 on Rinkeby so verification is invoked more often (Eric)
  - Coordinate with Yondon after the verification code updates are tested in devenv
- Sketch design and begin discussion around saving goclient state and restoring after restarts (Josh)
  - Video segments being transcoded
  - On chain events / last block (solve websocket instability issue)
  - Josh to create an organizing issue to kick things off for this project
- Start talking with IPFS about gx and go-ipfs which is blocking basicnet PR; will be a maintenance headache. (Josh)
- Finish PR for enforcing segment length. Currently a WIP and not ready (Josh)

# Engineering Planning 3/25/2018

## Moderator / Notetaker: Josh Allmann
**Last Week**
- Underwent first full network deployment, genesis state, distribution dry run!
- Developed bug bounty program (Eric)
- Documented Launch deployment checklist (Yondon)
- Networking protocol changes (Josh)
- Pariticipation UI and infrastructure built (Josiah)
- Website updates (Josiah)

**This Week**
- **Emphasis is on stability fixes and documentation.**
- Decision and set up around ETH node used for distribution. Related to this is handling any connection breakage (Yondon)
- Make sure we are set up to handle any halting during the distribution and that we can recover (Yondon)
- Continue to formalize deployment and genesis checklist (Yondon)
- Work on fixing verification-computation-solver (Yondon, Eric)
  - Potential additional changes needed here related to latest transcoder changes for LPMS
- Test the revocation of the vesting contract (Eric)
- Multisig key management decisions (Doug)
- Set protocol parameters (Doug)
- Set up a mainnet synced archive node (Eric)
- Revisit devenv to get it up to date, update the developer doc along the way. (Eric)
- Update ReadTheDocs in support of launch (Doug to coordinate, but might need some team input)
- Add call reward functionality in the CLI
- Investigate transcoder behavior under load (Josh)
- AWS Infra review (Josiah and Eric)
- Participation UI content udpdates (Josiah)
- Possibly: Transcoding level selection in chroma player, bonding UX (Josiah)


# Engineering Planning 3/19/2018

## Moderator / Notetaker: Josiah Savary
**Last Week**
- Reviewed participation content strategy, created participation repo + issues, and kept team unblocked (Doug)
- Wrote response to audits (Yondon)
- Pushing some recommended updates from this release to next; PRs outstanding (Yondon)
- Wrote backend token distro scripts (Yondon)
- Major problem solved for transcoder stability -- too many file descriptors (Eric)
- Protocol updates seem to be in good shape. The pieces are in and does everything that we agreed on (Josh)
- Made updates to the basicnet testing setup; PR outstanding (Josh)
- Deployed testable / working version of serverless participation api (Josiah)

**This Week**
- **Big Goal**: e2e registration / distro dry-run by Thursday 3/19 (Doug)
- Detailed step-by-step checklist for mainnet deployment (Doug)
- Need to come up with mainnet protocol parameters (Doug)
- Add additional logic for failure conditions / tracking progress in distro scripts (Yondon)
- Focus on Basicnet (Josh)
  - Integrating go client
  - Get tests passing
  - Continue to create and comment on issues concerning potential med/long-term complications regarding our network topology
- Continue to improve transcoder stability (Eric)
  - Infura WebSocket connections still unstable...trying different strategies to compensate. Potential solutions are linked to persisting livepeer node state.
  - Verifiers -- need scripts to monitor, restart, and manually verify specific events
- Create proposal for bug bounty program (Eric)
- Security checklist (Eric)
- Continue discussions with distributed contributors (Nicolas, etc) (Eric)
- Iterate on participation frontend / API (Josiah)
- Prepare for Berlin hackathon (Josiah)
  - Update LivepeerJS documentation
  - Publish latest LivepeerJS packages to npm

# Engineering Planning 3/12/2018

## Moderator / Notetaker: Eric Tang

### Network Launch
**Last Week**
* Finished ToB audit
* Publish path decentralization post (Doug)
* Script for processing registered account balances and compute airdrop amounts (Yondon)

**This Week**
* Create ToB audit response, make changes according to the audit (Yondon)
* Finish up deployment for the explorer (Josiah)
* Json web tokens proposal (Josiah)
* Backend API for the airdrop app (Josiah)
* Captcha research (Let’s help Josiah on this)
* Complete airdrop distribution infrastructure including any necessary architectural updates with goal of having a setup that is easy to do dry runs with by EOD Thursday (Yondon)
* Run through and document operational/key management workflow for the airdrop distribution, protocol deployment and protocol upgrades (I think @Eric got started with this as it relates to the use of a multisig a few weeks ago) (Yondon)
* Get transcoders to run consistent transcoding, claiming, verification (Eric)
* Transcoder stability (Eric + Yondon)
  * Panic fd - https://github.com/livepeer/go-livepeer/issues/289
  * Transcoder as broadcaster does work but no one knows streamIDs - https://github.com/livepeer/go-livepeer/issues/284
  * Log ETH tx for debugging - https://github.com/livepeer/go-livepeer/issues/271
  * Node crash due to concurrent map read/write - https://github.com/livepeer/go-livepeer/issues/246
  * Maintain transcoder state (this is probably least priority this week since it is not just a bug fix and is a feature to   * recover from crashes or going offline) - https://github.com/livepeer/go-livepeer/issues/269
* Networking protocol change (Josh)


# Engineering Planning 3/5/2018

## Moderator/Notetaker: Yondon Fu

### Protocol
**Last Week**
* Support external audit - received initial weekly report and went through the read out with ToB (Yondon/Eric)
* Improve test coverage to 100% - improved branch coverage a good amount, not at 100% due to quirks of coverage tool used, but at a good place right now until audit completes (Yondon)
* Improve protocol documentation - received some helpful feedback from ToB on where to add some clarifying documentation, but did not get to actual writing. Holding off on this until audit completes to prioritize other engineering tasks (Yondon)
* Verification strategy - discussed briefly, but there are not any immediate actionable items until we re-focus on this area (Josh)

**This Week**
* Support external audit (Yondon)
* Document potential change to use a provided broadcaster address instead of a job creator's address when creating a job in an issue (Yondon)

### Go Client
**Last Week**
* ETH client related bug fixes (Yondon)
* Eric will coordinate network protocol changes - there needs to be more security analysis and threat modeling here, but the consensus is that what we have right now is ok and we can do more thorough analysis at a later point once we consider other changes (Eric)
* Eric to document how basicnet works today (Eric)
* Basicnet analysis, documentation. Hope to fix bugs as we go along. Develop a plan for the basicnet, in the short and medium term. (Josh)
* Merge transcoder PR (Josh)
* New release version of go-livepeer node (Eric)

**This Week**
* Goal: improve stability for the end-to-end system (broadcast -> transcode -> validate -> slash, round progression)
* Start implementation for proposed basicnet change (Josh)
* Discuss delayed broadcasting proposal - https://github.com/livepeer/go-livepeer/issues/316 - this is not urgent, but the issue is there to solicit feedback this week (Everyone)
* Transcoder node stability bug fixes to try to prevent crashes as much as possible (Yondon)
    - Panic fd - https://github.com/livepeer/go-livepeer/issues/289
    - Transcoder as broadcaster does work but no one knows streamIDs - https://github.com/livepeer/go-livepeer/issues/284
    - Log ETH tx for debugging - https://github.com/livepeer/go-livepeer/issues/271
    - Node crash due to concurrent map read/write - https://github.com/livepeer/go-livepeer/issues/246
    - Maintain transcoder state (this is probably least priority this week since it is not just a bug fix and is a feature to recover from crashes or going offline) - https://github.com/livepeer/go-livepeer/issues/269
* Issue clean up for go-livepeer to close issues known to be fixed already (Yondon)
* Stability for the verification computation solver, the daemon sometimes crashes (Yondon)

### Protocol Explorer
Overall, was very ambitious. Wrote a ton of code and made good progress on most tasks, but didn’t really finish any. There were are a lot of architectural patterns and refactoring I realized would be necessary groundwork for the tasked enhancements, so I focused on those. (Josiah)

**Last Week**
* Not started
    - Chroma: Video Player - Playlist Selection (ABR)
    - Update ETH faucet button
* Done
    - Form handling patterns (react-final-form)
    - Tracking Global unsubmitted transaction status (TransactionStatusContainer / React Context)
    - Pulling modals from inside view to being their own views (consume TransactionStatusContainer data)
    - Deduplicated a lot of shared code, added updated type annotations (queries, util functions)
    - Added Round type and currentRound query to GraphQL schema
* In-progress Explorer enhancements:
    - Claim Earnings - Button (done) + Transaction Modal
    - Withdraw Stake - Button (done) + Transaction Modal
    - Withdraw Fees - Button (done) + Transaction Modal
    - Add transaction mutations GraphQL schema
    - Transcoder “pending” stats

**This Week**
* Continue Explorer enhancements & deploy (Josiah)
* PRs! Schedule an introduction? - Trying out weekly PR that commits are pushed to throughout the week (Josiah)

### Misc
**Last Week**
* None

**This Week**
* Airdrop mechanism (Doug)
    - Working on messaging and the right way to communicate the process to the community
    - Working on preparing blog post drafts for publishing
    - Working with Josiah on UX
    - Interesting token distribution model to look at for reference is MakerDAO - not straightforward to join the community, but once you overcome the hurdle and technical education, you're welcomed with open arms into a tight knit community with many incentive aligned stakeholders

# Engineering Planning 2/26/2018
### Protocol
**Last Week**
* Truebit collaboration: compile ffmpeg into wasm, set up a repo similar to truebit scrypt repo (Yondon/Josh)
* Improve test coverage to 100% (Yondon)
* Got started on making progress here, but did not complete it
* Update transcoder pool to 20 with 10 active on Rinkeby (Eric) - I’ll do it today (Monday)

**This Week**
* Support external audit (Yondon + Eric)
* Improve test coverage to 100% (Yondon)
* Improve protocol documentation (Yondon)
* Update transcoder pool to 20 with multisig transaction (Eric)

### Go Client
**Last Week**
* Debug transcoder inactivity issue (Eric) - did not finish
* Code review for ffmpeg transcoder PR (Eric)
* Further work on transcoder PR; addressed comments, added tests (Josh)

**This Week**
* Bug fix - Transcoder Round Initialization stops (Yondon)
* Eric will coordinate network protocol changes (Eric)
* Eric to document how basicnet works today (Eric)
* Basicnet analysis, documentation. Hope to fix bugs as we go along. Develop a plan for the basicnet, in the short and medium term. (Josh)
* Merge transcoder PR (Josh)

### Protocol Explorer
**Last Week**
* Feedback for bond task flow (everyone)
* Task flows for Unbond, ClaimEarning, WithdrawStake, WithdrawFee (Josiah)
* Token distribution experience depending on discussions this week, not expected to be fully designed by eow (Josiah)
* Update sdk binding (Eric coordinate with Josiah)

**This Week**
* Education as “work”. Client-validated. How do we begin to create this content?
* Secondary mechanism to “prove humanity” (captcha? Multi-factor? tokens?)
* Chroma: Video Player - Playlist Selection (ABR)
* Prioritize Explorer Enhancements (bold means prioritize for this week)
  * **Claim Earnings - Button + Transaction Modal**
  * **Round Initialization - Navbar Status**
  * **Withdraw Stake - Button + Transaction Modal**
  * **Withdraw Fees - Button + Transaction Modal**
  * Pending Price/Cut/Fees
  * Update ETH Faucet (external link)
  * Messaging - Coaches
  * Messaging - Info Icons + Explanatory Modals
  * Claim Earnings - Badge
  * Claim Earnings - Warning Modal
  * Round Initialization - Warning Modal
* Website redesign (Eric make sure to get asset from Brad)


### Misc
**Last Week**
* Public testnet deployment (Eric)
* Design feedback - deadline on Wednesday (Everyone)
* Token Distribution - feedback by Thursday morning (please review the email thread)
* Community call this week (Doug)
* Audit Instructions (Doug)
* Create actionable items from the ETHDenver recap, and capture in Github. (Doug)

#### Note:
* Validation strategy (Josh)
  * For now, we can go with something naive like comparing frame rates and bit rates, but are many ways to break that, both intentionally and unintentionally. So I think we really need to spend some time developing the metrics we're going to be validating, and incorporate that into our long-term planning. Doubt we'll get this right on the first try, either. Make sure we have flexibility built into the protocol to refine the validation strategy after launch.
* Protocol explorer chores - decided to delay to a later time
  * Pre-commit hooks for linting/formatting
  * CONTRIBUTING.md
  * CI - Testing
  * CI - Coverage
  * CI - Deployment / Publishing
  * CI - Code Quality

# Engineering Planning 2/20/2018
#### Protocol Explorer
* Feedback for bond task flow (everyone)
* Task flows for Unbond, ClaimEarning, WithdrawStake, WithdrawFee (Josiah)
* Token distribution experience depending on discussions this week, not expected to be fully designed by eow (Josiah)
* Update sdk binding (Eric coordinate with Josiah)

#### Protocol
* Truebit collaboration: compile ffmpeg into wasm,  set up a repo similar to truebit scrypt repo (Yondon/Josh)
* Improve test coverage to 100% (Yondon)
* Update transcoder pool to 20 with 10 active on Rinkeby (Eric)

#### Go-Client
* Debug transcoder inactivity issue (Eric)
* Code review for ffmpeg transcoder PR (Eric)

#### Misc
* Public testnet deployment (Eric)
* Design feedback - deadline on Wednesday (Everyone)
* Token Distribution - feedback by Thursday morning (please review the email thread)
* Community call this week (Doug)
* Audit Instructions (Doug)
* Create actionable items from the ETHDenver recap, and capture in Github. (Doug)

# Eng Planning 2/12/2018
### Protocol
* Continue to make progress on the milestone (we should be done before Doug & Yondon leave for Eth Denver)

### Protocol Explorer
* Task flows + wireframes for Claim, Bond, Unbond, ClaimReward (Josiah)

### Go-Client
* Better unit test coverage for transcoding (Josh)
* Final PR for ffmpeg transcoder (Josh)
* Found a cause of the bug in networking (Eric)

### Misc
* Eth Denver getting started guide (Everyone)
* Prep for Truebit collaboration next week (Yondon, Josh, Eric)
* Operations key management (Eric)
* Protocol / testnet deployment (Eric)


# Eng Planning 2/05/2018
### Protocol
Goal: Start external audit on 2/14
* Consensys security checklist (we didn't get to it last week, but got through a lot of other security audit todos) (Doug / Yondon)
* Continue working through issues found through the audit (Yondon)
* Internal security audit checklist (Eric)

### Protocol Explorer
* Wireframe for bonding/unbonding (Josiah)
* Basic bonding interface (Josiah)
* New UI/UX dev process / tools (Josiah)

### Go-Client
* Document new transcoding system so everyone else can learn the different components involved (Josh)
* New transcoder implementation (Josh)

### Misc
* Document [How we work](https://github.com/livepeer/project-management#how-we-work) (Doug)
* Start using [explorer project section](https://github.com/livepeer/livepeerjs/projects/1) to capture tickets for the explorer (Everyone)
* Use [Project Proposals](https://github.com/livepeer/project-management/projects/1) and [Livepeer Community Roadmap](https://github.com/livepeer/project-management/projects/2) to capture high-level thoughts/updates (Everyone)

# Eng Planning 1/29/2018
### Protocol
Goal: Start external audit on 2/14 (operation safe v-day)
* Consensys security checklist (Doug / Yondon)
* User acceptance security audit (Eric)
* Integration tests for user interactions (Yondon)
* Improve unit test coverage (Yondon)

### Protocol Explorer
* Finish transcoder election view (Josiah)
* Documentation for protocol explorer + js sdk (Josiah)

### Go Client
* Testing for segmenter ffmpeg integration (Josh)
* Remove transcoder ffmpeg dependency (Josh)

### Misc
* Ensure testnet uptime during this week's live broadcasts (Eric)


# Eng Planning 1/22/2018
### Protocol
Goal: Start Internal Audit
Action Items:
* 2 last code changes before code freeze for internal audit (Yondon)
  * Transcoding election fix
  * Enforce transcoder bonding
* Sanity checks around Livepeer Verifier (Doug / Yondon)
* Live contract update (Yondon)
* Doug to start internal audit
* Eric to do the checklist version of internal audit

### Protocol Explorer
* Transcoder view design session (Josiah)
* Transcoder view implementation (Josiah)

### Go Client
* ffmpeg project (Josh)
* Integration test plan for go-livepeer and go-livepeer-basicnet (Eric)
* Job assignment fix (Yondon)
* Upgrade IPFS to new version (Yondon Volunteered)

### Misc
* Timescale-accurate testnet protocol deployment (Yondon/Eric)
* Dockerize Livepeer (Joe)
* Auto-gen ABIs pushed to later
* Continuous deployment of web player pushed to later


# Eng Planning 1/16/2018
### Protocol
Goal: Prep for Internal Audit
Action Items:
* Testing - fee distribution, job being distributed to different transcoders, watch / slash, transcoder set rotation (Doug)
* Testing - seeing adaptive bitrate stream (Eric)
* Linter / compiler warnings (Yondon)
* Covergae testing (Yondon)
* Start internal audit this week

### Protocol Explorer
Goal: Continue to make progress on UI/UX
Action Items:
* Demo during community call on 1/18 (Josiah)
* Transcoder view, transcoder election (Josiah)
* Deploy a version to S3 (Josiah)

### Go Client
Goal: Stability
Action Items:
* Remove ffmpeg external dependencies (Josh)
* Bug fixes (Eric)
* Watcher (need a owner)

### MISC
* Currently the node loses all of its state when stopped.  Filed [an issue](https://github.com/livepeer/go-livepeer/issues/269)
* Deploy the test player at a different URL
* Continuous deployment of the web player
* Monitoring endpoint health, auto-restart
* Moving beyond using screen to run Livepeer in AWS
* Make logs available
* Auto-generated ABI repo
* Research integration test tools (Eric)
* Move testnet deploy key management to 1password (Eric)

# Eng Planning 1/8/2018

### Protocol
Goal: Internal Audit
Action Items:
* Simulating genesis state - Yondon
* Upgrade path (version number) - Yondon
* Internal audit checklist - Doug

### Protocol Explorer
* Profile view - Josiah
* Transcoder view - Josiah
* Deployment to S3 - Josiah

### Go Client
* Duplicate nonce bug - Yondon
* Standard SDK spec (golang and js sdk should have the same interface) - Yondon/Josiah
* Memory issue - Eric
* Error messages - Eric
* Bug squash - Eric

### Misc
* Ops - roles for different environments, key storage, etc (Eric to work with Joe offline)
* Protocol explorer next step: bond/unbond/deposit/withdraw/claim
* Video player next step: add resolution picker
* Go client next step: Eric to work on Jan release goal
* Postpone public testnet deployment until later time
