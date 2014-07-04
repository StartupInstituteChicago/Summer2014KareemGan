=begin
	
Here's one to start you off, sourced from Chris Pine's Learn to Program:

* 99 Bottles of Beer

Write a program which prints out the lyrics to that beloved classic, that field-trip favorite: 99 Bottles of Beer on the Wall.

Requirements:
* Should print out the lyrics to the command line.
* Each verse should be separate by a single blank line.
* Make sure pluralization is correct once you get down to 1 bottle of beer, and no more bottles of beer.
	
=end

class BottleSong

	attr_accessor :n

	def initialize(n)
		@n = n
	end

	def bottles(y)
    	(y.zero? ? "no more" : y).to_s << " bottle" << ("s" unless y == 1).to_s
	end

	def sing
		n.downto(0) do |i|
			puts "#{bottles(i).capitalize} of beer on the wall, #{bottles(i)} of beer."
			if i.zero?
				puts "Go to the store and buy some more, #{n} bottles of beer on the wall."
			else
				puts "Take one down and pass it around, #{bottles(i-=1)} of beer on the wall."
			end
			puts
		end
	end
end

class String
  def is_number?
    true if Float(self) rescue false
  end
end

puts("Hello, thank you for trying my wonderful app! Now we shall sing \"n\" Bottles of Beer!")
puts("Ideally people sing this song with 99 bottles of beer, but if you can't control your liquor then who am I to stop you!")
print("Enter the numbe of bottles of beer you want! ")
user_bottles = gets.chomp

if user_bottles.is_number?
	alcoholic = BottleSong.new(user_bottles.to_i)
	alcoholic.sing
else
	puts("Are you already drunk? Because you did not enter a valid number!")
end
