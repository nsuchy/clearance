rails_versions = %w(
  4.2
  5.0
  5.1
  5.2
)

rails_versions.each do |version|
  appraise "rails_#{version}" do
    gem "railties", "~> #{version}.0"
    if Gem::Version.new(version) >= Gem::Version.new("5.0")
      gem "rails-controller-testing"
    end
    gem 'rspec-rails', '~> 3.1'
  end
end

# Rails 6 pre-release testing
# Combine with above when 6.0 is final
appraise "rails_6.0" do
  gem "railties", "~> 6.0.0.beta"
  gem "rails-controller-testing"
  gem 'rspec-rails', github: "rspec/rspec-rails", branch: "4-0-dev"
  gem 'rspec-core', github: "rspec/rspec-core"
  gem 'rspec-mocks', github: "rspec/rspec-mocks"
  gem 'rspec-expectations', github: "rspec/rspec-expectations"
  gem 'rspec-support', github: "rspec/rspec-support"
end
