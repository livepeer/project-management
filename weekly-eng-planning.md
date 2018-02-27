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
