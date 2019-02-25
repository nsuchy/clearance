rails_versions = %w(
  4.2.0
  5.0.0
  5.1.0
  5.2.0
  6.0.0.beta
)

rails_versions.each do |version|
  appraise "rails_#{version[0..2]}" do
    gem "railties", "~> #{version}"
    if Gem::Version.new(version) >= Gem::Version.new("5.0")
      gem "rails-controller-testing"
    end
  end
end
