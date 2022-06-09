First thing is input



For now I think the best way is to just pull down the mismerged errors file manually onto the secured drive so we can easily access it, then if this works well figure out how to access Cygwin from the script, or put it onto the server where it can easily pull the file given its location



Second is getting prod data from sql



I think the best way would to take an array of MRN's from mismerged and write one sql query that gives us a second df that we can compare against

Third is the hardest part, and the crux of this rock, actually comparing the data





I'm not wholly convinced this will work/be good enough. I was feeling confident earlier as it seems so formulaic when we do it. My hesitancy comes from the fact that the dataloader already technically does this, which is why we have the file in the first place, but maybe we have expertise the devs didn't. This should be a lot of regex and try/if statements. Need to delve deeper here.

For testing, we're going to want to keep an eye out for files with real and false alarm mismerged errors, we should ask the whole team for that, but be especially vigilant on our failed load days. We can go ahead and fix them as normal for now, but we should make a list of the locations of them and whether they were real, so we can go back and see if the script comes to the same conclusion.



Once all that's done we can focus on usability, I was thinking of using a package to create a gui to run it, but it might also be that we put it on rundeck for people who don't have python properly installed which is a whole different issue.



I'd like to keep it clean looking, so once something is robust, let's refactor it into a function and throw it in a different file. I'll try and get a github set up in the next day or two, depending on how busy fails are today. Once that's good we can work on whatever, whenever. Let's just keep each other in the loop so we're not doing the same thing at the same time.