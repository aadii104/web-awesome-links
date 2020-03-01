# [ESLint](https://eslint.org/)

- Code linter for latest Javascript
- Flags all unnecessary errors/warnings. It's like local SonarQube

---

- [Configuring ESLint](https://eslint.org/docs/user-guide/configuring)
- [List of all available rules](https://eslint.org/docs/rules/)
- [Developer Guide](https://eslint.org/docs/developer-guide/)
- [Using ESLint with prettier](https://medium.com/@netczuk/your-last-eslint-config-9e35bace2f99)

## Writing custom linting rules for ESLint

> It is fairly straightforward writing custom rules for ESLint.

- ESLint uses [**AST**](https://en.wikipedia.org/wiki/Abstract_syntax_tree) for parsing through the code
- We will be using Esprima parser to understand the AST syntax of the code we will be linting [Link](http://esprima.org/demo/parse.html#)
  <br><br>
- Here is a fairly quick intro to the syntax of writing your rule [link](https://gist.github.com/jareware/7179093)
- Here are the API docs for ESLint [Working with rules](http://eslint.org/docs/developer-guide/working-with-rules)
- We will be using Yeoman Generator to simplify the process of creation of a rule.

> Install Yeoman generator as a global package using npm `npm i -g eslint-generator`

### Add your rule

- In the root directory of the project, type in following command `yo eslint:rule`
- That will start an interactive dialog, which will result in creation of skeletal file structure for the rule and its test-case.
- Edit the file and see it in action

### Using the custom rules in your project

- From the custom rules project directory, type `npm link`
- Link the rules for use inside your project, type `npm link <ProjectName>`
- [Working with plugins](https://eslint.org/docs/developer-guide/working-with-plugins)
- Go to the Project and install custom rules `npm i -D eslint-plugin-<ProjectName>`
- Edit .eslintrc to include your new rule for testing
