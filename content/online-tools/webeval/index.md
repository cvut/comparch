---
title:  "Web Evaluator for QtRvSim"
---

A web application for submission and evaluation of student (and also of the general public) solutions of [bonus RISC-V tasks](https://cw.fel.cvut.cz/wiki/courses/b35apo/en/homeworks/bonus/start) in [b35apo](../../courses/fel/b35apo/). The application takes a code snippet written in RISC-V assembly or C and runs it in QtRvSim using a custom wrapper written in Python. During the evaluation the correctness of the solution is checked by easily configurable testcases, all written in .toml format. After the evaluation is done, a task is scored based on the runtime of the program in cycles. This allows a bit of competition between the students.

In the current state, the evaluator is able to check the content of the registers and the state of memory at set addresses. A comparison of uart is also possible. Each of the testcases can be configured to be either private or public (if set to private the log does not show the trace of an error), with a separate testcase which is set to be a kind of a benchmark - to allow fair competition between different submissions. The system also allows for a custom Makefile to be included, with additional files to be present during compile time.

## Links

- [WebEvaluator](https://eval.comparch.edu.cvut.cz)

- The application has been presented on [Installfest 2024](https://installfest.cz/if24/), [Slides](/slides/if24slides-webeval.pdf), [Video](https://www.youtube.com/watch?v=1XQR8E8omCE&list=PLub6xBWO8gV8AG4kBn5W-QkMnTcdAPqvn&index=8). We also held a small hackathon during this event, which helped us to test the application and collect useful feedback.

- The application has also been used during education at [SpaceMaster](https://spacemaster.eu/) program in Kiruna, Sweden.

- [Source code (GitLab)](https://gitlab.fel.cvut.cz/b35apo/qtrvsim-eval-web)

## How to start

Head on over to the [registration page](https://eval.comparch.edu.cvut.cz/register) and create an account. Then select a task from the main page, write your solution and submit it. After the evaluation is done, you can see the results on the page task.

## Contact person

[Jakub Pelc](https://swpelc.eu/contact/)
