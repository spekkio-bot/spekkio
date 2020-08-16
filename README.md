# Spekkio
[![Server status](https://img.shields.io/website?down_color=red&down_message=offline&label=server&up_message=online&url=https%3A%2F%2Fjunha.netlify.com)](https://5ila6fw37k.execute-api.us-west-1.amazonaws.com/api)
[![Go Report Card](https://goreportcard.com/badge/github.com/spekkio-bot/spekkio)](https://goreportcard.com/report/github.com/spekkio-bot/spekkio)

*"I'm Spekkio, the Master of ~War~ GitHub!"*

Spekkio is a set of tools and services that delivers a better developer experience to teams on GitHub by automating tedious things.

## Available Scripts

### `run.sh`

To run the app, simply run `./run.sh`. You will need to do some [setup](https://github.com/spekkio-bot/spekkio/blob/master/src/README.md#first-time-setup) before you can run the app.

You can also navigate to `src/` and directly build / run the app there.

### `deploy.sh`

You can deploy the app to AWS Lambda with `./deploy.sh` - in a nutshell, this script will first build your app to `bin/`, then deploy your executable app to AWS if it built successfully.

Deploy settings are determined by `serverless.yml`.

## License

Licensed by the GNU General Public License, version 3.
