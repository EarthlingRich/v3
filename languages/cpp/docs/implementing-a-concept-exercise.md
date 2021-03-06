# How to implement a C++ concept exercise

This document describes how to implement a concept exercise for the C++ track. As this document is generic, the following placeholders are used:

- `<SLUG>`: the name of the exercise in kebab-case (e.g. `anonymous-methods`).
- `<NAME>`: the name of the exercise in snake_case (e.g. `anonymous_methods`).

Before implementing the exercise, please make sure you have a good understanding of what the exercise should be teaching (and what not). This information can be found in the exercise's GitHub issue. Having done this, please read the [C++ concept exercises introduction][concept-exercises].

To implement a concept exercise, the following files must be created:

<pre>
languages
└── cpp
    └── exercises
        └── concept
            └── &lt;SLUG&gt;
            ├── .docs
            │   ├── after.md
            │   ├── hints.md
            │   ├── instructions.md
            │   └── introduction.md
            ├── .meta
            │   ├── design.md
            │   ├── example.cpp
            │   └── example.h
            ├── CMakeLists.txt
            ├── &lt;NAME&gt;.cpp
            ├── &lt;NAME&gt;.h
            ├── &lt;NAME&gt;_test.cpp
            └── test
                ├── catch.hpp
                └── tests_main.cpp
</pre>

## Step 1: adding track-specific files

These files are specific to the C++ track:

- `<NAME>.h` and `<NAME>.cpp`. the stub implementation files, which is the starting point for students to work on the exercise.
- `CMakeLists.txt`: the C++ project file.
- `<NAME>_test.cpp`: the test suite.
- `.meta/example.h` and `.meta/example.cpp`: an example implementation that passes all the tests.
- `test/catch.hpp`: single-header testing library.
- `test/tests_main.cpp`: generates test main from test library.

## Step 2: adding common files

How to create the files common to all tracks is described in the [how to implement a concept exercise document][how-to-implement-a-concept-exercise].

## Step 3: add analyzer (optional)

Some exercises could benefit from having an exercise-specific [analyzer][analyzer]. If so, specify what analysis rules should be applied to this exercise and why.

## Step 4: custom representation (optional)

Some exercises could benefit from having an custom representation as generated by the [C++ representer][representer]. If so, specify what changes to the representation should be applied and why.

## Inspiration

When implementing an exercise, it can be very useful to look at already implemented C++ exercises. You can also check the exercise's [general concepts documents][reference] to see if other languages have already implemented an exercise for that concept.

## Help

If you have any questions regarding implementing the exercise, please post them as comments in the exercise's GitHub issue.

[analyzer]: https://github.com/exercism/cpp-analyzer
[representer]: https://github.com/exercism/cpp-representer
[concept-exercises]: ../exercises/concept/README.md
[how-to-implement-a-concept-exercise]: ../../../docs/maintainers/generic-how-to-implement-a-concept-exercise.md
[reference]: ../../../reference
