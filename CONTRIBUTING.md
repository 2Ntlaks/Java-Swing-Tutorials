# Contributing to Java Swing Tutorials

Thanks for your interest in contributing! Whether you're a fellow tutor, a student who found a typo, or someone who wants to add a new lesson — you're welcome here.

## How to Contribute

### Reporting Issues

- Found a typo, broken link, or incorrect code? Open an [issue](https://github.com/2Ntlaks/Java-Swing-Tutorials/issues).
- Include the lesson number and a brief description of the problem.

### Suggesting Improvements

- Have an idea for a new lesson topic (e.g., `GridLayout`, `JPanel`, `JMenuBar`)?
- Open an issue with the tag **suggestion** and describe what the lesson should cover.

### Submitting a New Lesson

If you want to write a new lesson, please follow these guidelines to keep the series consistent:

#### Lesson Structure

Every lesson should follow this format:

1. **Introduction** — What the student will learn and why it matters. Connect it to what they already know.
2. **Concept Explanation** — Explain the new concept clearly. Use analogies when helpful. Don't assume prior knowledge beyond what earlier lessons covered.
3. **Complete Code Example** — A full, runnable program. Students should be able to copy it, run it, and see it work.
4. **Line-by-Line Breakdown** — Walk through the important parts of the code. Explain *why*, not just *what*.
5. **Key Takeaways** — Bullet-point summary of the main concepts.
6. **Practice Exercises** — 5-8 exercises that range from "type it out and run it" to "build something new." Include at least one exercise that asks students to break something on purpose to understand what a piece of code does.

#### Writing Style

- **Be clear and direct.** Write like you're explaining to a friend, not writing a textbook.
- **Use `this` explicitly** when calling methods on the frame (e.g., `this.setSize()`, `this.add()`). This is a deliberate teaching choice throughout the series.
- **Show the full program** every time, not just snippets. Beginners need to see where everything goes.
- **Include screenshots** in the `screenshots/` folder. Name them with the lesson number prefix (e.g., `10-gridlayout-example.png`).
- **Add a solution file** in the `solutions/` folder with worked answers for exercises that involve code.

#### File Naming

- Lessons: `lessons/XX-topic-name.md` (e.g., `10-gridlayout.md`)
- Solutions: `solutions/XX-solutions-topic-name.md`
- Screenshots: `screenshots/XX-description.png`

#### Linking

- End your lesson with a link to the next lesson: `*Next: [Part XX -- Topic](XX-topic.md)*`
- Update the previous lesson's "What's Next" section to link to your new lesson.
- Add your lesson to the table in `README.md`.

### Pull Request Process

1. Fork the repository.
2. Create a branch with a descriptive name (e.g., `add-lesson-10-gridlayout`).
3. Make your changes following the guidelines above.
4. Test all code examples — every program should compile and run.
5. Submit a pull request with a clear description of what you added or changed.

## Code of Conduct

Be respectful. This is a learning resource. We're all here to help students understand Java Swing better.

## Questions?

Open an issue or reach out to [@2Ntlaks](https://github.com/2Ntlaks).
