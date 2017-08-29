# Coinbase Thing

> Because naming things is hard.

## Installation

```bash
git clone blah blah blah

# you should probably have rvm installed....
cd coinbase-thing

gem install bundler
bundle install

# run the server thing
rackup -p 8000

# test the thing
rspec -fd .
```

## Testing


## Discussion

We don't really need a whole library to make one HTTP request, but using the coinbase/exchange gem is simple. Also, y'all should really add `gem 'coinbase-exchange'` to the install section cause I had to look at the gemspec to find it. You need to hold developer's hands sometimes.

You should really document that `APIClient::orderbook` accepts `product_id` as a param cause I had to look at the code to see what it should be called. As soon as I have to look at the source code, a ton of developers have given up. You need to hold their hands sometimes.

I use `.reduce(&:+)` rather than `.sum` because it may not respect the `+` operator of BigDecimal.

Should use VCR for the tests, but it's unnecessary right now.
