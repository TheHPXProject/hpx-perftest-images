# HPX performance test images

This repository stores the plots that the HPX performance tests produce on the [LSU Rostam cluster](https://github.com/TheHPXProject/hpx/tree/master/.jenkins/lsu-perftests), so that the comments the CI posts on [HPX](https://github.com/TheHPXProject/hpx) pull requests can show them. GitHub comments can only show images that are hosted somewhere, and the Jenkins artifacts on Rostam are not publicly reachable.

The Jenkins `lsu-perftests` job pushes the images here. Please don't commit to this repository by hand.

## Layout

Each run adds one directory:

```
pr/<pull request number>/<build number>/<test name>_<index>.png
```

The `<index>` counts the measurements in the test's report. Each plot compares the distribution of the current measurement with the reference result.

## Links

Comments link to the images through the commit that added them, not through the branch, so that a later run can't change what an older comment shows:

```
https://raw.githubusercontent.com/TheHPXProject/hpx-perftest-images/<commit>/pr/<pull request>/<build>/<test name>_<index>.png
```

## Size

The history of this repository is occasionally replaced by a single commit with only the recent runs, to keep it small. The images in comments on older pull requests stop showing up after that.

## Access

The Jenkins job pushes with a deploy key that has write access to this repository only.

## License

Distributed under the Boost Software License, Version 1.0. See [LICENSE](LICENSE).
