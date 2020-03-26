# addons-github-issue-counts

Scripts for pushing add-ons specific github issue counts into influxdb. Uses github's GraphQL API and node-influx to push stats into influxdb easy graphing.

## Want to use this for your own project?

* Copy this and create your own repo. You probably don't want to fork this since you won't need to track the changes.
* Update the query and script in `bin/getGithubIssueCounts` to suit your needs.
* Be sure to update your event naming - see the prefix in `measurement`.
* Add the following tokens to a .env file (to test locally) or circle-ci if you are wanting to use Circle-ci's cron to push the stats into datadog (recommended).
    * Add `GH_TOKEN` you should set this to `public_access` (no scope) since this is most likely public data.
    * Add `INFLUX_DB_HOST`
    * Add `INFLUX_DB_PORT`
    * Add `INFLUX_DB_DATABASE`
    * Add `INFLUX_DB_USER`
    * Add `INFLUX_DB_PASSWORD`
* Check you're receiving data for your events in influx/grafana.
* When you're happy run this from Circl-ci and find interesting ways to to graph the data.
* If you make something cool with this please let me know!
