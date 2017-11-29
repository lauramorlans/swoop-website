# swoop-website

Jekyll based, served automatically from Github using the `gh-pages` branch.

## Local development:

Work on the correct branch:

`git checkout gh-pages`

Ensure you have the correct version of Ruby - see  [Requirements](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#requirements)
(When installing bundler, you may need to use `sudo gem install bundler`)

Then install all the required libs for Jekyll.

`bundle install`

If that worked fine, you can view your site using:

`bundle exec jekyll serve`

# Troubleshooting

There were some problems installing then nokogiri gem on Glen's Mac.  To resolve, you need to install a missing dependency:

`brew install libxml2`

Then install the nokogiri gem 'manually'.  This command works for me, you may need to change the version of nokogiri - read the error output from bundle install to see what it tried to install and grab the version from that, replacing '1.6.8.1' in the command below with the right version.
Also, the path to the libxml2 library includes may differ on your Mac - check the long path and edit as appropriate.

`sudo gem install nokogiri -v '1.6.8.1' -- --with-xml2-include=/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.12.sdk/usr/include/libxml2 --use-system-libraries`
