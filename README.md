# Zero Knowledge Proofs: Privacy Without Compromise

Materials for the zero-knowledge proofs talk. Aimed at beginners to intermediate. You don't need any cryptography
or blockchain background.

> **Coming up:** [Burning River CyberCon](https://burningrivercybercon.com), November 14th at 78th Street Studios,
> Cleveland.

## Start here

| | |
| --- | --- |
| Slides (view online) | [Google Slides](https://docs.google.com/presentation/d/1eU7H5Cip_vMas13f9hSaq-xbiXw1a6bu/edit) |
| Slides (download) | [`slides/Zero-Knowledge-Proofs.pptx`](slides/Zero-Knowledge-Proofs.pptx) |
| Live demo | [ZKCord](https://github.com/michael-bey/zkcord): a Discord bot that verifies age and nationality from a passport without seeing the passport |
| Interactive explainer | [eli5.zksync.io](https://eli5.zksync.io) |

## What's a zero-knowledge proof?

A cryptography tool that lets you:

1. **Prove a statement is true**: "this user is over 18"
2. **Without revealing the secret behind it**: their birthday, January 1, 2008
3. **In a way that is extremely hard to fake**: cryptographers call this *soundness*

## Talk outline

1. **The problem with KYC.** Know Your Customer checks mean companies collect and store passport photos and
   personal data, which makes them a valuable target for hackers. AI makes fake IDs and fake selfies easier to make.
   Long onboarding flows drive users away.
2. **How ZK proofs work.** An illustrated walkthrough, adapted from material by Matter Labs and Marcin Michalski.
3. **Practical examples.**
   - [ZKPassport](https://zkpassport.id): reads the government-signed NFC chip in your passport and makes a proof
     on your phone.
   - QuarkID: digital credentials issued by a government (for example, a vaccination certificate) that you can
     prove facts about without showing the whole document.
   - [Semaphore](https://semaphore.pse.dev): prove you're a member of a group without revealing which member.
     Used for private voting, anonymous feedback and anonymous chat.
4. **Demo:** ZKCord.

## Demos

### Fooling a liveness check (slide 14)

A short clip of a video-game character's face getting through an online "prove you're a real person" selfie
check. It shows why a photo or video of you is getting weaker as proof of who you are.

- [Watch on Google Drive](https://drive.google.com/file/d/1KuH124QlL_SzBo5p82nfZldIyZVkxwEn/view) or
  download [`videos/liveness-check.mp4`](videos/liveness-check.mp4)

### ZKPassport walkthrough (slide 28)

A screen recording of the [ZKPassport web demo](https://demo.zkpassport.id) proving someone is 18 or older. The
browser's network tab is open the whole time, so you can watch what actually gets sent.

- [Watch on Google Drive](https://drive.google.com/file/d/1yf5g8k87GD-ZN4RBvz1rE9ENQdApRG4s/view) or
  download [`videos/zkpassport-demo.mp4`](videos/zkpassport-demo.mp4)

### ZKCord

A Discord bot that gives server members roles (18+, nationality, region like the EU) from a ZKPassport proof.
The server learns only the facts it asked for. The name, date of birth, passport number and photo stay on the
member's phone.

- Code: [github.com/michael-bey/zkcord](https://github.com/michael-bey/zkcord)
- Try it on your own server: [zkcord.vercel.app](https://zkcord.vercel.app) and the
  [setup guide](https://zkcord.vercel.app/admin-guide)
- What the server sees and doesn't see:
  [How verification works](https://github.com/michael-bey/ZKCord/wiki/How-verification-works)

## Learn more

### Beginner

- [ZK Proofs, explained like you're five](https://eli5.zksync.io): the interactive explainer the talk's
  illustrations come from
- [Zero Knowledge Proofs: An illustrated primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/),
  Matthew Green
- [Zero-knowledge proof](https://en.wikipedia.org/wiki/Zero-knowledge_proof) on Wikipedia

### Intermediate

- [ZK Visualizer](https://www.zkvisualizer.com): watch a real proof get built step by step in your browser, from
  circuit to constraints to polynomials to verification
- [An approximate introduction to how zk-SNARKs are possible](https://vitalik.eth.limo/general/2021/01/26/snarks.html),
  Vitalik Buterin
- [ZK Learning MOOC](https://zk-learning.org): free university course with lectures and exercises
- [ZKProof](https://zkproof.org): community standards and reference documents

### Build something

- [Noir](https://noir-lang.org): a Rust-like language for writing ZK programs, used by ZKPassport
- [Circom](https://github.com/iden3/circom): a widely used language for writing ZK circuits
- [ZKPassport docs](https://docs.zkpassport.id): add passport verification to your own app
- [Semaphore docs](https://docs.semaphore.pse.dev): anonymous group membership

## Contact

Michael Benich

- [LinkedIn](https://www.linkedin.com/in/michaelbenich)
