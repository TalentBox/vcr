source :rubygems
gemspec

gem 'excon', :git => 'git://github.com/geemus/excon.git', :ref => '1bd9b8167a090335c82f3a3c5c84fb654822c467'

group :development do
  # patron and em-http-request can't install on JRuby, so we have to limit their platform here.
  platforms :ruby do
    gem 'patron',           '~> 0.4.15'
    gem 'em-http-request',  '~> 0.3.0'
    gem 'curb',             '0.7.15'
    gem 'typhoeus',         '~> 0.3.3'
  end

  platforms :jruby do
    gem 'jruby-openssl'
  end
end

# Additional gems that are useful, but not required for development.
group :extras do
  gem 'guard-rspec'
  gem 'growl'
  gem 'relish', '~> 0.5.0'
  gem 'fuubar'
  gem 'fuubar-cucumber'

  platforms :mri do
    gem 'rcov'
    gem 'rb-fsevent'
  end

  platforms :mri_18, :jruby do
    gem 'ruby-debug'
  end

  platforms :mri_19 do
    gem 'ruby-debug19'
  end unless RUBY_VERSION == '1.9.3'
end

