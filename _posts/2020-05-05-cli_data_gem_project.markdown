---
layout: post
title:      "CLI Data Gem Project"
date:       2020-05-05 16:18:41 +0000
permalink:  cli_data_gem_project
---


      For my CLI Data Gem project, I chose to scrape the New York Times' Bestsellers List for Paperback Fiction. My program lists the 15 novels by title and author, the user is then asked which novel he/she would like to learn more about and depending on the number they would choose (1 -15), the selected novel's publisher, weeks spent on the list and synopsis are shown. The user is asked whether he/she would like to take another look at the list and, depending on their answer (Y/N), the program returns to the list of novels or ends.
      Any time I approach something that'll end with an assessment, I prepare myself to be in immediate confrontation with all of my weaknesses. In the case of this project, it became apparent that I have a tendency to make a single method responsible for multiple tasks. I think my intial reasoning is that if I keep the amount of methods to a minimum, I can explain the whole process to myself in a couple of statements. I point my finger to a couple of moves and it makes universal sense. For example: 
			
			```   def show_info
    puts "Which novel would you like to learn more about? (Enter 1-15)"
    user_choice = gets.strip
    puts "-----"
    if user_choice.to_i <= 15 && user_choice.to_i > 0
      puts "Publisher: " + "#{@novels[user_choice.to_i - 1].publisher}"
      puts @novels[user_choice.to_i - 1].weeks_on_list
      puts "Synopsis: " + "#{@novels[user_choice.to_i - 1].synopsis}"
    else 
      show_info 
    end 
  end ```
	
	     If the method stays true to its name, #show_info should really begin at puts "puts "Publisher: " + "#{@novels[user_choice.to_i - 1].publisher}."" The code preceeding this statement should be written a separate method indicating (solely) validation, defined with a parameter for the user's input. #valid?, or something akin to that name, can be nested within show_info (also with a parameter for the user's input), preferably in the first line. If valid? == true, then show_info; this would be ideal. 
			 Accompanying this change would be the removal of " puts "Which novel would you like to learn more about? (Enter 1-15)"" & "user_choice = gets.strip" from either method after refactoring since both commands are simply prerequisites for either method. They seem to fall more in line, as they individually stand, in the order that would be exhibited in the CLI class' call method. I'll edit to include this piece of code's refactoring once I enter the final stages of my project.
	
