# Binary Hopfield Networks

- A toy experiment on memory recall as competing patterns are added to a Hopfield network
- I just wanted to see how new associations would affect recall and what the changes in similarity and energy would say

## What I did

- 7 scenes, each with an old pattern (ex), a new pattern (benji), and a background context (bg)
- Converted images into 32 × 32 binary patterns (−1/+1)
- Initially trained the network on the old patterns
- Added new patterns over 30 randomly selected scene updates (keeping the initial weight contributions)
- After each update, used a noisy context cue to test retrieval with asynchronous updates

## Questions

- Does recall reach a fixed point?
- How similar is the output to the old/new patterns?
- Does it reconstruct either pattern exactly?
- How do the old/new target energies change during learning?
- Are the patterns fixed points in the final weights?

## What happened

In the saved run:

- 29 of 30 retrievals reached a fixed point!
- But none actually reconstructed its exact corresponding old/new pattern
- All new associations had lower final energy compared to old associations.
- None of the 14 patterns were a fixed point under the final weights.

So settling, pattern preferences, and exact reconstructions are all different things. An output can be closer to new than old without being a good reconstruction of the new association. And lower energy doesn't ensure that the cue will retrieve the association.
