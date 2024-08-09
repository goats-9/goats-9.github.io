---
title: "Artificial Intelligence in Competitive Programming"
date: 2023-12-08T06:17:46+05:30
draft: false
toc: true
tags: ['competitive-programming', 'artificial-intelligence', 'ai', 'cp']
---

One of the benchmarks for progress in Artificial Intelligence (AI) is games
usually played by humans, such as Minesweeper, Chess, Jeopardy and even
StarCraft. By pitting AI against the best players in the world in these games,
we can assess how well these AI models perform in a real-world game situation.
It is no mean feat to create an AI that can play games such as Chess better than
any human opponent. So when Google DeepMind came up with engines such as
[AlphaZero and
MuZero](https://deepmind.google/technologies/alphazero-and-muzero/) that
[outdid](https://www.science.org/doi/10.1126/science.aar6404) more well-known
chess engines such as IBM Stockfish 8, it drew a huge reaction from the chess
and chess programming community.

Another such wave might be starting in the competitive programming (CP)
community. Competitive programming is (in my opinion) a fun sport where
contestants have a fixed amount of time to code solutions to sets of problems in
general-purpose programming languages like C, C++, Python, Rust, Java and so on,
under constraints on input, runtime limit and memory limit. Many online sites
such as [Codeforces](https://codeforces.com),
[CodeChef](https://www.codechef.com/) and [CodeDrills](https://codedrills.io/)
have online judges that compile and run submitted code in many programming
languages on multiple public and private test cases to verify if the problem has
been solved by the contestant. Codeforces have a rating system where your rating
is a result of your performance in live contests hosted regularly on that
platform. Perhaps the most prestigious on-site CP contest is the International
Collegiate Programming Contest [(ICPC)](https://icpc.global).

## AlphaCode and CP

Google DeepMind have now come up with another AI model, AlphaCode
[(AC)](https://alphacode.deepmind.com/), and more recently, AlphaCode 2
[(AC2)](https://storage.googleapis.com/deepmind-media/AlphaCode2/AlphaCode2_Tech_Report.pdf),
powered by [Gemini](https://deepmind.google/technologies/gemini/). AC2 reads the
problem statement and outputs the solution code, using transformer-based
language models to generate codes and filter out the eventual solution code.
Validation on Codeforces using newer problems than in the training dataset show
that AC2 performs at the 85th percentile on this platform (between Expert and
Candidate Master). This has evoked a good number of
[reactions](https://codeforces.com/blog/entry/123035) on Codeforces, with some
members voicing their concerns.

## Implications for CP

Instead of going through the technical details that can be found in the original
paper as well as the technical report for AC2, I will try to summarize the
reactions of the community as of the day of typing this post.

1. Some members observed that AC2 could solve problems rated over 3000 in one
   go, but struggled to solve lower rated problems that appear in division 2
   A-C. This led to concern over test data leakage. A clarification tweet from
   [Rémi Leblond](https://twitter.com/RemiLeblond/status/1732677521290789235)
   tries to explain this anomaly. A pertinent point raised is that the public
   test cases for the high rated problem were strong, so passing those testcases
   legitimately would almost certainly receive an AC verdict, making it an
   outlier in this way. This is something humans like myself experience when
   solving a tougher problem in a live setting where the public tests are hard
   to pass, so I feel that some of the anomalies are valid to an extent. But it
   remains to be seen how that factors into assessing or benchmarking AC2's
   performance.

2. Other members, including the Codeforces founder [Mike
   Mirzayanov](https://codeforces.com/profile/MikeMirzayanov) welcomed the
   progress made by AC2 and are eager to see its growth in performance. Still
   other members also drew parallels to the [IMO Grand
   Challenge](https://imo-grand-challenge.github.io/). I feel that this is a
   long way to go, especially because there are fewer topics in CP than in
   mathematics. Perhaps, a better assessment would come in a live round.

3. Few comments pointed out the impact on platforms like Codeforces, talking
   about problem validation and competitive integrity. This is by far the
   **most** plaguing problem for regular CPers like myself, with many of my own
   contacts through CP harping on this point. It is an absolutely valid concern,
   and other members pointed out the anomalies listed above as well as believe
   that at this stage, AC2 in a live setting would perform even worse than on
   the validation (which was done using virtual contests).

## Conclusion

From what I can see above, I think there is one question on everyone's mind:
_Can AC2 replicate its performance in a live contest?_ An answer to this
question will definitely quench a lot of question marks in the community, and
make clear the progress of AI in PSA-based settings like CP.
