require 'rubygems'
require 'bundler'
require 'yaml'

require File.join(File.dirname(__FILE__), '_rake', 'deploy')
require File.join(File.dirname(__FILE__), '_rake', 'generate')
require File.join(File.dirname(__FILE__), '_rake', 'helper')
require File.join(File.dirname(__FILE__), '_rake', 'new')
require File.join(File.dirname(__FILE__), '_rake', 'serve')
require File.join(File.dirname(__FILE__), '_rake', 'setup')

BASE_DIR = File.dirname(__FILE__)
SOURCE_DIR = ENV.fetch('source', 'source')
CONFIG_FILE = File.join(BASE_DIR, SOURCE_DIR, '_config.yml')
CONFIG = YAML.load_file(CONFIG_FILE) if File.exists?(CONFIG_FILE)

# Ensure all directories exist
[ '', 'pygments_code', 'stash' ].each do |dir|
  FileUtils.mkdir_p(File.join(BASE_DIR, '_tmp', dir))
end

task :default => :dev
