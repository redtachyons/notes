# Bundler included by default
* weired bundler bug
* No longer have to do gem install bundler soon after installing ruby

# Block level rescue
https://bugs.ruby-lang.org/issues/12906

* In ruby you can rescue excptions in functions and classess without explicit begin statement as below
```ruby
def method_name
  ...
rescue
  ...
end
```
In ruby 2.5, you can do the same in blocks as well

```ruby
[0,1,2,3,4,5].map do |nubmer|
  number/0
rescue
  0
end
```

# Integer square root
```ruby
Integer.sqrt(16)
```

# Removed suffix and prefix in easy way
```ruby
"redpanthers".delete_prefix("red")
=> "panthers"
```
"redpanthers".delete_suffix("panthers")
=> "red"
```

```

# Active support to ruby core
# Array.prepend and Array.prepend
https://bugs.ruby-lang.org/issues/12746
* Human way of thinking
append is aliased to push
prepend is aliased to unshift


# Transform keys
https://bugs.ruby-lang.org/issues/13583

* Was available in active support
* Transform keys in the hash

For instance if you want to convert all keys in the hash to string, you can use
```ruby
 {a: 1, b: 2}.transform_keys {|key| key.to_s}
```
```ruby
 {a: 1, b: 2}.transform_keys(&:to_s)
```
