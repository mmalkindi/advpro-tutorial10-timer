# Tutorial 10 - Part 1: Timer

## 1.2 Understanding how it works

![Print outside of spawner](img/outside_spawner_print.png)

We can see that the line outside of the spawner (`Alkindi's Komputer: hey hey`) is printed before the lines in the async function.
This is because the print function for said line is run in the main thread before `executor.run` is called,
which is responsible for running the async function thats in the spawner's task queue.
Once the async function is called, the line `Alkindi's Komputer: howdy!` is printed with the other line (`Alkindi's Komputer: done!`)
printed 2 seconds later.
