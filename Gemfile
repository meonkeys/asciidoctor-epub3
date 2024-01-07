# frozen_string_literal: true

source 'https://rubygems.org'

# Look in asciidoctor-epub3.gemspec for runtime and development dependencies.
gemspec

group :optional do
  # epubcheck-ruby might be safe to be converted into runtime dependency,
  # but could have issues when packaged into asciidoctorj-epub3
  gem 'epubcheck-ruby', '~> 5.1.0.0'

  # Kindlegen is unavailable neither for 64-bit x86 macOS nor for ARM
  # Also, skip JRuby on Windows for now. See https://github.com/jruby/jruby/issues/7171
  gem 'kindlegen', '~> 3.1.0' unless RUBY_PLATFORM =~ /darwin/ || (Gem.win_platform? && RUBY_ENGINE == 'jruby')
end
