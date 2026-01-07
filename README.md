# Coverband Demo

A Rails 7.1 application demonstrating how to use [Coverband](https://github.com/danmayer/coverband) for production code coverage tracking.

## Quick Start

### Prerequisites

- Ruby 3.1+
- Redis (for Coverband storage)
- SQLite3

### Setup

```bash
bundle install
rails db:create db:migrate
rails server
```

Visit `http://localhost:3000` to see the app.

### View Coverage Data

The Coverband web UI is mounted at `/coverage`:

```
http://localhost:3000/coverage
```

## Live Demo

Visit the live demo site: [https://coverband-demo.herokuapp.com/](https://coverband-demo.herokuapp.com/)

## Features Demonstrated

- **Code Coverage Tracking**: See which lines of code are executed in production
- **View Tracking**: Monitor which views/templates are rendered
- **Route Tracking**: Track which routes are accessed
- **Dead Code Detection**: Identify unused code paths

## Configuration

Coverband is configured in `config/coverband.rb`:

```ruby
Coverband.configure do |config|
  config.store = Coverband::Adapters::HashRedisStore.new(Redis.new(url: ENV['REDIS_URL']))
  config.track_views = true
  config.track_routes = true
end
```

## Running with JRuby

This application supports both CRuby (MRI) and JRuby. To run with JRuby:

```bash
# Update .ruby-version to jruby, or:
rvm use jruby
bundle install
bundle exec rails s
```

## Deployment

### Heroku

The demo site is hosted on Heroku. Basic setup follows the [Heroku Rails Guide](https://devcenter.heroku.com/articles/getting-started-with-rails7).

Required add-ons:
- Redis (for Coverband data storage)
- PostgreSQL (for production database)

## Theme

The UI uses a Material Design Bootstrap theme based on:
- [Hero Rails](https://github.com/frontted/hero-rails)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a Pull Request

## Related Projects

- [Coverband](https://github.com/danmayer/coverband) - The main Coverband gem
- [Coverband Service](https://github.com/coverband-service) - Hosted Coverband service
