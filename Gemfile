# If you have OpenSSL installed, we recommend updating
# the following line to use "https"
source 'http://rubygems.org'

gem "middleman", "~> 3.4.0"

gem 'middleman-deploy', '~> 1.0' # Requires fix referenced here: https://github.com/middleman-contrib/middleman-deploy/issues/114#issuecomment-168139237

gem "middleman-livereload" # Live-reloading plugin

# Cross-templating language block fix for Ruby 1.8
platforms :mri_18 do
  gem "ruby18_source_location"
end
