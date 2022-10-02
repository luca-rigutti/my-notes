# Testing

Working in progress, this is only a test not ultimated.

---

In the file (docker of Wordpress)[./docker.md] you can setup the image with already the [WP CLI](https://wp-cli.org/).
With it, you can generate the test files with `wp scaffold plugin-tests sample-plugin` [doc page](https://developer.wordpress.org/cli/commands/scaffold/plugin-tests/).

Then you need to setup with this [guide](https://make.wordpress.org/cli/handbook/misc/plugin-unit-tests/), then with `phpunit` you can run the tests.


[^1]: https://www.smashingmagazine.com/2017/12/automated-testing-wordpress-plugins-phpunit/
[^2]: https://mklasen.com/adding-and-using-wp-cli-in-a-docker-compose-setup/
[^3]: https://carlosguzman.dev/running-phpunit-tests-in-a-wordpress-plugin-with-docker/