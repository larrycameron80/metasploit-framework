source 'https://rubygems.org'
# Add default group gems to `metasploit-framework.gemspec`:
#   spec.add_runtime_dependency '<name>', [<version requirements>]
gemspec name: 'metasploit-framework'

# separate from test as simplecov is not run on travis-ci
group :coverage do
  # code coverage for tests
  gem 'simplecov', '>= 0.16.1'
end

group :development do
  # Markdown formatting for yard
  gem 'redcarpet'
  # generating documentation
  gem 'yard'
  # for development and testing purposes
  gem 'pry'
  # module documentation
  gem 'octokit'
  # Metasploit::Aggregator external session proxy
  gem 'metasploit-aggregator' if [
    'x86-mingw32', 'x64-mingw32',
    'x86_64-linux', 'x86-linux',
    'darwin'].include?(RUBY_PLATFORM.gsub(/.*darwin.*/, 'darwin'))
  gem 'google-protobuf', "3.5.1" if [
    'x86-mingw32', 'x64-mingw32',
    'x86_64-linux', 'x86-linux',
    'darwin'].include?(RUBY_PLATFORM.gsub(/.*darwin.*/, 'darwin'))
  gem 'grpc', "1.8.3" if [
    'x86-mingw32', 'x64-mingw32',
    'x86_64-linux', 'x86-linux',
    'darwin'].include?(RUBY_PLATFORM.gsub(/.*darwin.*/, 'darwin'))
end

group :development, :test do
  # automatically include factories from spec/factories
  gem 'factory_girl_rails', '>= 4.9.0'
  # Make rspec output shorter and more useful
  gem 'fivemat'
  # running documentation generation tasks and rspec tasks
  gem 'rake'
  # Define `rake spec`.  Must be in development AND test so that its available by default as a rake test when the
  # environment is development
  gem 'rspec-rails', '>= 3.7.2'
  gem 'rspec-rerun'
end

group :test do
  # Manipulate Time.now in specs
  gem 'timecop'
end
