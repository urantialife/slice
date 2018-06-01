<h1 vertical-align="middle">Slice
    <a targe="_blank" href="https://twitter.com/home?status=Slice%20%E2%80%94%20Python's%20extended%20slice%20syntax%20for%20JavaScript%20%40IntoliNow%20%23Intoli%0A%0Ahttps%3A//github.com/intoli/slice">
        <img height="26px" src="https://simplesharebuttons.com/images/somacro/twitter.png"
            alt="Tweet"></a>
    <a target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A//github.com/intoli/slice">
        <img height="26px" src="https://simplesharebuttons.com/images/somacro/facebook.png"
            alt="Share on Facebook"></a>
    <a target="_blank" href="http://reddit.com/submit?url=https%3A%2F%2Fgithub.com%2Fintoli%2Fslice&title=Slice%20%E2%80%94%20Python%27s%20extended%20slice%20syntax%20for%20JavaScript">
        <img height="26px" src="https://simplesharebuttons.com/images/somacro/reddit.png"
            alt="Share on Reddit"></a>
    <a target="_blank" href="https://news.ycombinator.com/submitlink?u=https://github.com/intoli/slice&t=Slice%20%E2%80%94%20Python%27s%20extended%20slice%20syntax%20for%20JavaScript">
        <img height="26px" src="media/ycombinator.png"
            alt="Share on Hacker News"></a>
</h1>

<p align="left">
    <a href="https://circleci.com/gh/intoli/slice/tree/master">
        <img src="https://img.shields.io/circleci/project/github/intoli/slice/master.svg"
            alt="Build Status"></a>
    <a href="https://github.com/intoli/slice/blob/master/LICENSE">
        <img src="https://img.shields.io/badge/License-BSD%202--Clause-blue.svg"
            alt="License"></a>
    <a href="https://www.npmjs.com/package/slice">
        <img src="https://img.shields.io/npm/v/slice.svg"
            alt="NPM Version"></a>
</p>


A JavaScript implementation of Python's extended slice syntax.


```javascript
import { range, SliceArray } from 'slice';


// Populate a list from 1 through 100.
const outputs = range(1, 100 + 1);

// Replace every 3rd element with 'Fizz'.
outputs[[3 - 1,,3]] =
  Array(Math.floor(100 / 3))
    .fill('Fizz');

// Replace every 5th element with 'Buzz'.
outputs[[5 - 1,,5]] =
  Array(Math.floor(100 / 5))
    .fill('Buzz');

// Replace every (3 * 5)th element with 'Fizz Buzz'.
outputs[[3 * 5 - 1,,3 * 5]] =
  Array(Math.floor(100 / (3 * 5)))
  .fill('Fizz Buzz');

// Tada!
console.log(outputs);
```


## Development

To get started on development, you simply need to clone the repository and install the project dependencies.

```bash
# Clone the repository.
git clone https://github.com/intoli/slice.git
cd slice

# Install the dependencies.
yarn install

# Build the project.
yarn build

# Run the tests.
yarn test
```

There is also a separate test suite which generates many thousands of slice operations on the fly in Python.
These generated operations are then applied in JavaScript to confirm that everything works as expected.
The auto-generated tests can be run with the `yarn test:generated` command.


## Contributing

Contributions are welcome, but please follow these contributor guidelines:

- Create an issue on [the issue tracker](https://github.com/intoli/slice/issues/new) to discuss potential changes before submitting a pull request.
- Include at least one test to cover any new functionality or bug fixes.
- Make sure that all of your tests are passing and that there are no merge conflicts.
- You agree to assign the copyright for any contributions to Intoli, LLC.


## License

Slice is licensed under a [BSD 2-Clause License](LICENSE) and is copyright [Intoli, LLC](https://intoli.com).
