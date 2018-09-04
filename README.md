# addons-github-issue-counts

Scripts for pushing add-ons specific github issue counts into datadog. Uses github's GraphQL API and datadog web API to push stats into datadog for easy graphing.

![Screenshot showing github issue counts in DataDog](screenshots/dash-for-issue-counts.png?raw=true "Screenshot showing github issue counts in DataDog")

## Want to use this for your own project?

* Copy this and create your own repo. You probably don't want to fork this since you won't need to track the changes.
* Update the query and script in `bin/getGithubIssueCounts` to suit your needs.
* Be sure to update your event naming - see the prefix in `metrics.init`.
* Add the following tokens to a .env file (to test locally) or circle-ci if you are wanting to use Circle-ci's cron to push the stats into datadog (recommended).
    * Add `GH_TOKEN` scope should be minimal since this is most likely public data.
    * Add `DATADOG_API_KEY` (request this key from a datadog admin).
* Check you're receiving data for your events in datadog.
* When you're happy run this from Circl-ci and find interesting ways to to graph the data.
* If you make something cool with this please let me know!
