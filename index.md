# H1 - There Can (well, _should_) Be Only One!

![why i oughta](https://user-images.githubusercontent.com/19803303/226885307-27825b9b-b855-439e-94c6-5b1942a85fef.gif)

### H3 - For Kicks

```ruby
dial_book = {
  'newyork' => '212',
  'newbrunswick' => '732',
  'edison' => '908',
  'plainsboro' => '609',
  'sanfrancisco' => '301',
  'miami' => '305',
  'paloalto' => '650',
  'evanston' => '847',
  'orlando' => '407',
  'lancaster' => '717'
}

# Get city names from the hash
def get_city_names(somehash)
  return_string = ''
  somehash.each_key { |entry_key| return_string << (entry_key.to_s + "\n") }
  return_string
end

# Get area code based on given hash and key
def get_area_code(somehash, key)
  somehash[key] ? "The area code for #{key} is #{somehash[key]}." : 'Invalid choice'
end

# Execution flow
loop do
  puts 'Do you want to lookup an area code based on a city name? (Y/N)'
  answer = gets.chomp.downcase
  break if answer != 'y'

  puts
  puts 'Which city do you want the area code for?'
  puts
  city_names = get_city_names(dial_book)
  puts city_names
  puts
  print 'Enter your selection: '
  selection = gets.chomp.downcase
  answer = get_area_code(dial_book, selection)
  puts
  puts answer
  puts
end
```

###### H6 - Wasting Everyone's Time

- [x] Start GitHub Foundations course
- [x] Revise Mardown
- [ ] Complete GitHub Foundations course
