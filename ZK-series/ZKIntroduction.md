# "THE WAY" OF PRIVACY: INTRODUCTION TO ZERO KNOWLEDGE PROOFS(ZKPs).
This article explains the introductory concept of  zero-knowledge proofs (ZKPs), deep explaination on how ZKP works with an illustrative case study.
Taliored for both technical and non technical ZK enthusism
### Why Privacy??

 I have the worst handwritten signature ever- It's everything else but scribbled and worse than a deterministic salt with no nonce or deadline to it, XD. Everytime i sign in the bank, I think: " imagine i have loads of money here and i'm using something so insecure to verify my identity. This centralised, non cryptographical encripted, controlled fiat bank got my back?, maybe not XD". Let's forget about my poor signature for a moment, But Have you ever wondered why we need to tell so much information just to verify a single fact or signature?

What if there was a way I could prove "This is really Hamid(bad sig guy!)" without showing my signature at all? Or prove "I have enough money" without revealing my exact balance?

This is exactly what Zero Knowledge solves and allow us to do.
### WHAT IS ZERO KNOWLEDGE PROOFS(ZKPs)? 
Zero Knowledge proof(ZKPs) are cryptographical method or proofs to prove a specific data/information hold a true value without revealing any part of that data/information. It's like proving i own this bank account with giving out any form of information(including my bad signature) account.

For every ZKP action/Tasks, there must be an actor(s). in the case of ZK there are 2 actors/roles:
- Prover(Hamid): The Prover actor is responsible for generating ZK proofs of a valid data without revealing the data itself.  They generate a proof based on this knowledge that the verifier can check. In a bank case study, This is Hamid(bank customer) claiming to know the signature to access his without actually revealing his signature.
- Verifier(Cashier): The Verifier Actor is responsible for verifying a ZK proof od a data is truly valid, without gaining any information about the data itself. using a bank case study, this is the cashier validating ola(customers) claim/proof without learning anything about his signature. 

For ZK to work properly, It needs 3 properties to always hold true value:
- Completness: If the input sent by the prover is valid, the proof must always convince the verifier.
- Soundness: If the input submitted by the prover is false, it must be pratically Impossible for the proof to trick the verifier.
- Zero Knowledge: If the statement is true, then the verifier learns nothing else about the information apart from the fact that the statement is true

# NON-INTERACTIVE AND INTERACTIVE Zero Knowledge Proofs(ZKPs)


| Aspect                  | Interactive ZKPs(prover🔁verifier)           | Non-Interactive ZKPs(prover➡⬅verifier)   |
|-------------------------|----------------------------------------------|--------------------------------------------|
| Communication Pattern   | - Multiple rounds of communication           | - Single message containing proof          |
| Verification Process    | - Verifier actively participates             | - Verifier can check proof independently   |
| Prover-Verifier Dynamic | - Requires back-and-forth challenges         | - No further interaction needed            |
| Blockchain Suitability  | - Not suitable for blockchain applications   | - Ideal for blockchain applications        |
| Implementation Challenge| - Need for repeated interaction              | - Reduces need for communication           |
| Verification Mechanism  | - Verifier must be present during proof      | - Anyone can verify proof at any time      |
| Practical Application   | - Limited in distributed systems             | - Can be stored and verified later         |

To further explain this, let's take a scenario of two Cases:
- Interactive ZKPs(1st CASE): I(bank customer) needs to verify my identity to access my account, i have a multiple dialogue with the cashier, with No/zero data being revealed. This is an Interactive ZKPs
- Non-Interactive ZKPs(2nd CASE): same case i need to verify my identity to access my account, i as a prover have a direct single verication dialogue with the cashier, with No/zero data being revealed. This is a Non-Interactive ZKPs.


- types of ZKP systems 
  - STARKS 
  - SNARKS examples are 
    - groth
    - plonk
  -  the Trusted Setup in Zero-Knowledge Proofs: analogy for this, imagine a tresure city where hidden gem boxes are made my hamid, every on this city have access to this boxes, but hamid made duplicate keys for every one in the city to verify themselves, only ligimate keyholder have access. hamid also have a dagerous master key that must not be seen unless other city governor can copy and make their own boxes, we dont want that ahaha 
     -  toxic waste: master key to be destroyed. like tau they can create fake proof that can be used to breach security system 
     -  common reference string: this is like the rules of security verification thhat the prover(villagers) and box(verifiers) use to verify the proof. it is the paramenters or values that has a point in the elliptic curves. 
     -  structured Reference String (SRS): instead of src, where the rules are different and commonly less structured, the src is having precision-engineered rules that fit together in a specific way. the src comes from the ellitic curves derived from the power of tau t
     - Multi-party Computation (MPC): instead of having just hamid making these gem boxes, you have multiple parties/hand smith welding this boxes and ensuring that the toxic waste is passed in well. imagine that all this special welders have they own part of the master key add their own randomness to it.
   - GROTH16 trusted set up
   - plank trusted set up
   - groth16 trusted set 
  - components oof ZKPs(SNARK)
  - Creating a zero-knowledge proof: steps are: arithemetization, proof creation,verification
    - frontend: constrant system that represent that is use to represent the problem mathematically.
    - backend: is a verifying system that generates and verify proofs based on the circuits
  - Arithemetization: converts mathematical 
  - Domain-specific languages. 
    - NOIR, ACIR
    - CIRCOM RICS
    - CAIRO ACIR
if you read to the end of this article, thank you very much. i must confess im not a writer, I'm only following feymann learning technique. Feel free to be my critics if there is any misinformation. if you are dev and find ZK development intresting, check out my NOIR series, THE WAY of Noir zero to hero. feel free to contribute and call out any issue.


references- https://medium.com/@bhaskark2/understanding-zero-knowledge-proofs-part-1-verifiable-computation-with-zk-snarks-ba6cbb8e6001
