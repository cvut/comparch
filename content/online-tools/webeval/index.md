---
title:  "Web Evaluator for QtRvSim"
---

A web application for submission and evaluation of student (and also of the general public) solutions of [bonus RISC-V tasks](https://cw.fel.cvut.cz/wiki/courses/b35apo/en/homeworks/bonus/start) initially prepared for the [B35APO](../../courses/fel/b35apo/) bachelor Computer Architectures course. The code snippet written in RISC-V assembly or C is entered through the web interface, and it is compiled by [QtRvSim](https://github.com/cvut/qtrvsim) internal assembler or GCC and then run in [QtRvSim](https://github.com/cvut/qtrvsim) using a wrapper application written in Python. During the evaluation, the correctness of the solution is checked by easily configurable test cases, all written in .toml format. After the evaluation, a task is scored based on the program's runtime in CPU cycles or other metrics (i.e., cache misses). The sorted listing of successful solutions allows a bit of competition between students in addition to bonus points received for the correct results. The last and the best-scored student submissions are kept in the database, the same as the obtained scores, listed in global and per event/class/institution scoreboards.

In the current state, the evaluator can check the registers' content and the memory region's final state at set addresses. Injection of data into memory region specified by address or symbol defined in the tested program is also possible (sequence to sort, which is unknown to the student, for example). A comparison of UART output to reference text is also possible. Each of the test cases can be configured to be either private or public (if set to private, the log does not show the trace of an error), with a separate test case, which is set to be a kind of benchmark - to allow fair competition between different submissions. The system also allows for a custom Makefile to be included, with additional files to be present during compile time.

The only hash of the e-mail address provided during registration is stored for comparison with the hash of the e-mail address used for password recovery. The address is used to send a password reset e-mail during the password recovery, but it is never stored in the database. We hope no GDPR measures apply to us or other organizations interested in running our evaluation system on their server.

The code can be analyzed and developed locally or [online](https://comparch.edu.cvut.cz/qtrvsim/app) in [QtRvSim](https://comparch.edu.cvut.cz/qtrvsim/app). The cache, pipeline, and other parameters must be set according to the task description in the Web Evaluator.

The tasks are sorted from introductory ones (i.e., simple value addition solved by three instructions inserted before ebreak) to more advanced sorting algorithm implementation in RISC-V assembly or C programs for processing data incoming from UART and printing the results similarly.

## Links

- [WebEvaluator](https://eval.comparch.edu.cvut.cz)

- The application has been presented on [Installfest 2024](https://installfest.cz/if24/), [Slides](/slides/if24slides-webeval.pdf), [Video](https://www.youtube.com/watch?v=1XQR8E8omCE&list=PLub6xBWO8gV8AG4kBn5W-QkMnTcdAPqvn&index=8). We also held a small hackathon during this event, which helped us to test the application and collect useful feedback.

- The application has also been used during education at [SpaceMaster](https://spacemaster.eu/) program in Kiruna, Sweden.

- [Source code (GitLab)](https://gitlab.fel.cvut.cz/b35apo/qtrvsim-eval-web)

## How to Start

Head on over to the [registration page](https://eval.comparch.edu.cvut.cz/register) and create an account. Then select a task from the main page, write your solution and submit it. After the evaluation is done, you can see the results on the page task. The page is not reloaded automatically for now. Use the page reload button, please.

## Contact Persons

- [Jakub Pelc](https://swpelc.eu/contact/) - the project author
- [Pavel Pisa](https://cmp.felk.cvut.cz/~pisa/) - the B35APO lecturer and computer architectures teaching coordinator at CTU FEE
