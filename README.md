# Magic::Link
Short description and motivation.

## Usage
How to use my plugin.

## Installation
Add this line to your application's Gemfile:

```ruby
gem 'magic-link'
```

And then execute:
```bash
$ bundle
```

Or install it yourself as:
```bash
$ gem install magic-link
```

configure your Devise user class if it isn't User
```ruby
# config/initializers/magic_link.rb
Magic::Link.configure do |config|
  config.user_class = "Customer"
end
```

Add `sign_in_token` and `sign_in_token_sent_at` to Customer

mount the engine
```ruby
mount Magic::Links::Engine, at: '/'
```

include helper so links in layout continue working
```ruby
class ApplicationController < ActionController::Base
  helper Magic::Link::ApplicationHelper
end
```

## Contributing
Contribution directions go here.

## License
The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
