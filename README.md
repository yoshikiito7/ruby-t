Welcome to the AWS CodeStar sample web service
==============================================

This sample code helps get you started with a simple Sinatra web service
deployed by AWS Elastic Beanstalk.

What's Here
-----------

This sample includes:

* README.md - this file
* .ebextensions/ - this directory contains the configuration files that allows
  AWS Elastic Beanstalk to deploy your application
* Gemfile - Gem requirements for the sample application
* config.ru - this file contains configuration for Rack middleware
* server.rb - this file contains the code for the sample service
* spec/ - this directory contains the RSpec unit tests for the sample application

Getting Started
---------------

These directions assume you want to develop on your local computer, and not
from the Amazon EC2 instance itself. If you're on the Amazon EC2 instance, the
virtual environment is already set up for you, and you can start working on the
code.

To work on the sample code, you'll need to clone your project's repository to your
local computer. If you haven't, do that first. You can find instructions in the
AWS CodeStar user guide.

1. Install bundle:

        $ gem install bundle

2. Install Ruby dependencies for this service:

        $ bundle install

4. Start the Sinatra development server:

        $ bundle exec ruby server.rb

5. Open http://127.0.0.1:4567/ in a web browser to view your service.

What Do I Do Next?
------------------

Once you have a virtual environment running, you can start making changes to
the sample Sinatra web service. We suggest making a small change to server.rb
first, so you can see how changes pushed to your project's repository are automatically
picked up and deployed to the Amazon EC2 instance by AWS Elastic Beanstalk. (You can watch
the progress on your project dashboard.) Once you've seen how that works, start developing
your own code, and have fun!

To run your tests locally, go to the root directory of the sample code and run the
`rspec` command, which AWS CodeBuild also runs through your `buildspec.yml` file.

To test your new code during the release process, modify the existing tests or add tests
to the `spec` directory. AWS CodeBuild will run the tests during the build stage of your
project pipeline. You can find the test results in the AWS CodeBuild console.

Learn more about the [RSpec API Documentation](http://rspec.info/documentation).

Learn more about AWS CodeBuild and how it builds and tests your application here:
https://docs.aws.amazon.com/codebuild/latest/userguide/concepts.html

Learn more about AWS CodeStar by reading the user guide. Ask questions or make
suggestions on our forum.

User Guide: http://docs.aws.amazon.com/codestar/latest/userguide/welcome.html

Forum: https://forums.aws.amazon.com/forum.jspa?forumID=248
