# Temporalis Contributing Guidelines

## Reporting bugs and proposing improvements

You can contribute to the development of Temporalis by reporting bugs. Please create an issue in the [bitbucket page](https://bitbucket.org/cardosan/brightway2-temporalis/issues) and describe the problem. Use a short and descriptive title for the issue. Ideally describe what you expected to happen vs. what actually happend. You can also add the output of the debug window or console if there is an error message related to the bug.

Also if you have general proposals or improvement ideas for Temporalis, create an issue in the [bitbucket page](https://bitbucket.org/cardosan/brightway2-temporalis/issues) .

## Pull requests

If you want to propose changes to the code or the documentation, just open a [pull request](https://www.atlassian.com/git/tutorials/making-a-pull-request). Fork the [Temporalis repo](https://bitbucket.org/cardosan/brightway2-temporalis), apply the changes in your forked repository and open a pull requests from there. Please also add a short description of what your PR accomplishes.

In the ideal case, you also write the test(s) for the new features that you add (see below).

## Running and writing tests

If you want to check whether your changes break anything essential, you can run the automated tests. This requires some additional packages.

You can then run the tests inside the repo running: `pytest`. 

Check out the tests that are already present in the `tests` folder for inspiration and examples.
