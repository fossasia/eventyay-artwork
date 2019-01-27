# PSLab iOS

[![Build Status](https://travis-ci.org/fossasia/pslab-iOS.svg?branch=development)](https://travis-ci.org/fossasia/pslab-iOS)
[![Gitter](https://badges.gitter.im/fossasia/pslab.svg)](https://gitter.im/fossasia/pslab?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/dd728d91bb5743ff916c16c1251f8dd5)](https://www.codacy.com/app/praveenkumar103/pslab-iOS?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=fossasia/pslab-iOS&amp;utm_campaign=Badge_Grade)
[![Mailing List](https://img.shields.io/badge/Mailing%20List-FOSSASIA-blue.svg)](mailto:pslab-fossasia@googlegroups.com)

This repository holds the iOS App for performing experiments with [PSLab](https://pslab.io/). PSLab is a tiny pocket science lab that provides an array of equipment for doing science and engineering experiments. It can function like an oscilloscope, waveform generator, frequency counter, programmable voltage and current source and also as a data logger. Our website is at https://pslab.io

## Communication

Please join us on the following channels:
* [Pocket Science Channel](https://gitter.im/fossasia/pslab)
* [Mailing List](https://groups.google.com/forum/#!forum/pslab-fossasia)

## Roadmap
 - [x] First we need to get communication between Android App and PSLab working.
 - [ ] Implement Applications and expose PSLab Hardware functionality to the user.
 - [ ] Implement Functionality to Perform Experiment using PSLab Hardware Device.

## Features
|   **Feature**    |                    **Description**                    |   **Status**    |
|------------------|-------------------------------------------------------|-----------------|
|   Home Screen    | Show status and version of PSLab device               |  		 TBD       |
|   Instruments    | Exposes PSLab instruments like Oscilloscope, etc      | 		 TBD       |
|  Oscilloscope    | Shows variation of analog signals                     | 		 TBD       |
|   Multimeter     | Measures voltage, current, resistance and capacitance | 		 TBD       |
| Logical Analyzer | Captures and displays signals from digital system     | 		 TBD       |
|  Wave Generator  | Generates arbitrary analog and digital waveforms      | 		 TBD       |
|   Power Source   | Generates programmable voltage and currents	   | 		 TBD       |
|    Lux Meter     | Measures the ambient light intensity                  | 		 TBD       |

# How to set up the iOS app in your development environment

### Requirements

- iOS 12.0+
- Xcode 10.0+

### Development Setup

Before you begin, you should already have the Xcode downloaded and set up correctly. You can find a guide on how to do this here: [Setting up Xcode](https://developer.apple.com/xcode/)

##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Steps to install Cocoapods (one time installation)

- Run `sudo gem install cocoapods` to install the latest version of cocoapods. To install cocoapods from HomeBrew, `brew install cocoapods`.

-  Next, run `pod setup` for setting up cocoapods master repo. You may include `--verbose` for more descriptive logs.
**NOTE:** This might take a while to setup depending on your network speed.

### Setting up the iOS Project

1. Download the _pslab-iOS_ project source. You can do this either by forking and cloning the repository (recommended if you plan on pushing changes) or by downloading it as a ZIP file and extracting it. OR
```
$ git clone https://github.com/fossasia/pslab-iOS.git
```

2. Navigate to the unzipped folder and run `pod install`.

3. Open `Pslab.xcworkspace` from the folder.

4. Build the project (⌘+B) and check for any errors.

5. Run the app (⌘+R).and test it.

## Setup to use PSLab with iOS App
To use PSLab device with iOS, you need to have the Apple Lightning connector. Connect PSLab device to iOS Phone via Lightning connector. Rest is handled by App itself.

## Contributions Best Practices

### Code practices

Please help us follow the best practice to make it easy for the reviewer as well as the contributor. We want to focus on the code quality more than on managing pull request ethics.

 * Single commit per pull request
 * Reference the issue numbers in the commit message. Follow the pattern ``` Fixes #<issue number> <commit message>```
 * Follow uniform design practices. The design language must be consistent throughout the app.
 * The pull request will not get merged until and unless the commits are squashed. In case there are multiple commits on the PR, the commit author needs to squash them and not the maintainers cherrypicking and merging squashes.
 * If the PR is related to any front end change, please attach relevant screenshots in the pull request description.

#### How to `git squash`?

As a tip for new developers those who struggle with squashing commits into one, multiple commits may appear in your pull request mostly due to following reasons.

 * Intentionally adding multiple commit messages after each change without just `git add`ing.
 * Updating the current branch with the remote so a merge commit takes place.

Despite any reason, follow the steps given below to squash all commits into one adhering to our best practices.

 * Setup remote to upstream branch if not set before;

`$ git remote add upstream https://github.com/fossasia/pslab-iOS.git`

 * Check into the branch related to the pull request

`$ git checkout <branch-name>`

 * Perform a soft reset to retain the changes while removing all the commit details

`$ git reset --soft upstream/development`

 * Add files to the staging area

`$ git add <file paths or "." to add everything>`

 * Create a new commit with a proper message following commit message guidelines

`$ git commit -m "tag: commit message"`

 * If you have already made a pull request,

`$ git push -f origin <branch-name>`

### Branch Policy

We have the following branches
 * **development**
	 All development goes on in this branch. If you're making a contribution,
	 you are supposed to make a pull request to _development_.
	 Make sure it passes a build check on Travis.

 * **master**
   This contains the stable code. After significant features/bugfixes are accumulated on development, we move it to master.


### Code style

* Please follow the guides and code standards: [Swift Style Guide](https://google.github.io/swift/)
* Please follow the good iOS development practices: [iOS Good Practices](https://github.com/futurice/ios-good-practices)

## License

This project is currently licensed under the Apache License 2.0. A copy of [LICENSE](LICENSE) is to be present along with the source code. To obtain the software under a different license, please contact FOSSASIA.
