---
layout: post
title:      "CLI Project 1- Scraping"
date:       2020-01-29 19:34:55 +0000
permalink:  cli_project_1-_scraping
---

My name is Ashley, and this blog is about my CLI Portfolio Project. The first one. This process was frustrating, stressful, exhilirating, and exciting. It took me longer than the others of my cohort to be honest. But, lets move past this and into my thought process.

As I thought about what I wanted to do my project on, I ran various ideas through my head. Ultimately, I decided on something to do with mushrooms. Why? Because for the area I live in, there is a lot of different kinds of mushrooms. And mushroom hunting is a huge thing around here. People use it to make extra money, for some it is their job, and for others its enjoyable. But, to be able to mushroom hunt, you need to be able to identify the mushrooms. Most mushrooms fall in certain families where as others haven't been classified yet. Thankfully, the ones that grow around my area are classified in families. And most of those families can lead you to be able to find out if the mushroom is safe to eat, toxic, or doesn't really do anything but not recommended to eat. So, my project narrows it down to show the kingdom, family, phylum, class, order, and genus. Those each make it easier to find out exactly what type of mushroom you are dealing with.

And now.....TO THE CODE!!! 

First things first, I needed something that could parse the HTML. I went with Nokogiri. Which has the following requirements:

*Provides a CLI (Command Line Interface)

*Command Line Interface must provide access to data from a web page.

*The data provided must go at least one level deep that shows the user a list of available data as well as be able to drill down into a specific item.

*Use good OO design patterns. You should create a collection of objects — not hashes to store your data.
Your project should not be too similiar to the Ruby final projects as Tic-Tac-Toe with AI and Student Scraper.

**## Let’s show how to built my CLI Data Gem project in the following steps:

**## Step 1 Install your gem in your terminal

bundle gemCLI-Mushrooms

This gem provides a Command Line Interface(CLI) to data scraped from a public website for user to choose which information he wanted to get a list.

**## Step 2 Creating my code

The way I did it was manually in VSCode. In my lib folder I created a file called mushroom_scraper.rb. There I put int the information as a hash. I wanted this information to be pulled from the website for the user to be able to see it. 

Here is the code I used. 

```
require 'pry'
require_relative "../spec/spec_helper.rb"
class MushroomScraper
    def self.scrape_from_wikipedia(url)
        doc = Nokogiri::HTML(open(url))
        mushroom_info = {
                :name => doc.css("th").first.text.strip,
                :kingdom => doc.css("div.kingdom a").text,
                :phylum => doc.css("div.phylum a").text,
                :klass => doc.css("div.class a").text,
                :order => doc.css("div.order a").text,
                :family => doc.css("div.family a").text,
                :genus => doc.css("div.genus a").text
        }
        mushroom = Mushroom.new_from_wikipedia(mushroom_info)

       
    end 
end
```
As you can see, I required pry as well as the spec_helper.rb file. Which, in all honesty I did after I had created this. I know...backwards!!! But, besides that, this shows which categories I wanted my scraper to show. 

I, then, made my mushroom_spec file. Which would show in more lengthy code what I wished it to achieve.

```
require_relative '../spec/spec_helper.rb'

describe Mushroom do

    let!(:mushroom) {Mushroom.new}

    context 'properties' do
         
       
       it "has a name" do 
            mushroom.name = "Name"
            expect(mushroom.name).to eq("Name")
        end

        it "has a kingdom" do
            mushroom.kingdom = "Kingdom"
            expect(mushroom.kingdom).to eq("Kingdom")
        end

        it "has a phylum" do           
            mushroom.phylum = "Phylum"
            expect(mushroom.phylum).to eq("Phylum")
        end
        
        it "has a klass" do            
            mushroom.klass = "Class"
            expect(mushroom.klass).to eq("Class")
        end

        it "has a order" do            
             mushroom.order = "Order"
             expect(mushroom.order).to eq("Order")
        end

        it "has a family" do            
             mushroom.family = "Family"
             expect(mushroom.family).to eq("Family")
        end

        it "has a genus" do            
             mushroom.genus = "Genus"
             expect(mushroom.genus).to eq("Genus")

        end
    end
end
```

Once that was done, I set up my spec_helper.rb file. Whic was pretty much just things I needed to require so that the rest of my code (which I hadn't done yet at this point) would work.

```
require_relative'../lib/mushroom'
require "nokogiri"
require "open-uri"
```
With that out of the way, I still needed my classes and files to scrape from the URL to retrieve that data. 
This is when I created my mushroom file. It contained the code that would make up my Mushroom class. The attribute accessors, the contructor, self method, and a custome constructor.

Now was the time for me to setup the choices, what I wanted the program to say to the user, and for it to bring forward the information requested. I only put in two choices to choose from. But, if I add to my code overall, I could eventually set it up to look up any kind of mushroom, with more details.

But, it wouldn't run without my start file. This being it:

```
#!/usr/bin/env ruby

require "./CLIMushrooms.rb"
#require_relative "../lib/mushroom.rb"
Intro_to_mushrooms.new.welcome
```
Using the shebang and the requirements, it had my code working. 

Throughout this process, I did get help. I will admit, I got stuck. My cohort lead and one of my cohort members helped me greatly. For that I am extremely thankful. Without them, I would not have gotten it done. It wasn't on time but there were extenuating circumstances that no one saw coming. Either way, I am glad to have done this project. 




