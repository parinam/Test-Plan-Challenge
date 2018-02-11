1. Each member of the team contributes to the quality of the product, collectively analyses and creates subtasks from the acceptance          criteria and evaluates any gaps in the requirements before starting the feature development.
2. Re-evaluate the estimation if there are changes in the requirements based on the discussion of point 2.
3. For faster delivery with high quality, the team (devs, QA, designers and Product Owners) can negotiate the tasks to be accomplished for    that feature.
  * Example:
       * Business would like performance testing as nice to have but something they can live with as long as it does not impact user’s              ability to perform on the application.
       * Low priority bugs can be taken up in later sprints.
      Above two points can go into the backlog to keep track of to-do’s.
4. Test cases are reviewed together as a team and the team provides sign-off on the test cases. This can go in parallel with development      of the feature.

### Follow fail fast approach (Trunk based development)
ONLY for toggled off features that is not ready for releases to end clients but the code can be pushed to production to minimize          merge/integration pain.

* Note: This works best when there are inter dependent teams releasing at the same time and avoids cherry picking later from the                   release branch if there is any critical bug.
    * Feature branches should be short-lived, no more than a day or two (doesn’t impede ability to release).
    * Feature branches should be first code reviewed for it to be merged to trunk (not a release branch)
    * Automation kicks off as part of continuous delivery once any feature branch is merged to trunk. This helps in failing fast by
      finding out defects on the integrated code earlier in phase.

### Toggled on features (That are exposed to end users)
* Example – Bugs (design, functional or non-functional), small ready features, small enhancements etc.
* Perform manual or automated testing on the feature branch and then its ready to be merged to master branch as this will go live soon.

*By following any of the two approaches above, release branch will be cut from the master branch and from there on no additional feature development can be merged to release branch. QA's will test on release branch for the release on pre-production environment. Any critical bugs if fixed on time will be added to hotfix-release-branch for testing again. There can be situations where release can go on hold.By following Trunk Based development it's less likely to get a critical bug but as lower environments are not exact copy of production environment, there is always chances of missing bugs. There is no 100% bug free application. <br/>
*This depends on team or org level. Business communicates to the end users about the scheduled release.
