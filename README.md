# craft-2019-impressions

Here's a compilation of reflections, rants and pure gibberish from CRAFT 2019 conference in Budapest.

## Keynotes

### When the universe calls, Pamela Gay

The interesting fact about this talk was that using the wisdom of the crowd it's possible to be as smart or smarter than a much smaller group of experts.
This was used on a project moon mappers where images of moon surface at very high resolution were tagged with craters and hills which was subsequently filled
to a ML algorithm to attempt to predict what is a crater or not. The result was still far from perfect.

A bit differently galaxy classification was done so at first researchers would classify galaxies but then that was fed to ML algorithms to predict the type of galaxy.

The things is that as our sensors got better the amount of data skyrocketed. For the recent observations where the entire Earth was changed into one giant telescope
the result was measured in petabytes and was sent by mail (as in the good old days).

Event though we can handle a lot of data today (or so I feel) we're basically still just scratching the surface when it comes to space.

### Cynefin, Dave Snowden

Cynefin is process framework for developing software. According to Snowden agile is now commoditized and ready to be evolved into something better.
On several talks I've heard the mention of *POST-Agile*. I guess people are as fed-up with all the buzzwords as I am.

I'd need to read a bit more on Cynefin to actually be more convinced of its practical utility. My impression was that it was more of an academic taxonomy rather than something I can go and apply in the workplace.

###  Deliberate Advice from an Accidental Career, Daniel Terhorst-North

I've listened to this talk at my first CRAFT conference and in my mind it's still fresh. The anecdotes stick. Or as Dan said "people will never forget how you made them feel".
As a techy I spend most of my time lost in technical details of one or another part of legacy and often tend to forget that a lot of significant problems are not really technical issues.

### Cultivating Instinct, Katrina Owen

There was a nice anecode on diagnosing sex of chickens which at some point in our history was a serious problems. Since its difficult(and expensive) to separate male and female chicks
people were trained to figure it out. However correctly separating one from another was largely a matter of experience and gut feeling rather than actual physical traits.
So the japanese devised a system, where a novice would learn together with an expert for two years and by the end they would be able to do it extremely well without really knowing how they do it.

It was shown that a group of random people could be trained to orient themselves on the map on a plane by showing them enough different exercises. 
It regularly happens that pilots land somewhere unexpected simply because they get lost.

Parallels were made with how programmers today solve problems where some people easily recognize complex problems at a glance while others puzzle for hours with no solution.
The question is how could we apply knowledge of learning the unconscious part of the brain faster than just learning by failing multitudes of times. 
I guess the mentioned exercism.io was an experiment in doing so. Need to check it out still.

## Talks I attended

### Persuading the Bear, Michael Nir

In this talk Michael talked about how to go about influencing others where there is no strong hierarchy.
Whenever people talk about agile and modern organization they emphasize the flatness of organizational charts.
Nobody however gives a sensible explanation of how this even can work in practice. 

Some ways of influencing others:
1. Give them the benefit of a doubt

	Essentially we're all in the same mess. If the company is doing bad everyone is influenced by that including people I might not like that much.
	I assume that means to show a bit of empathy towards everyone, rather than be held back by early judgements.

2. Adjust your behaviour

	According to Michael we normally tend to remain who we are regardless of the situation. We don't really adjust even though we can in order to influence others.
	Some basic options are to (from the BEAR):
		- push
		- pull back
		- withdraw

3. Repeat the last 3 words of the person who you're talking to.

	Repetition does feel really akwards but that is basically I'm not really used to doing that. Many speakers at the conference did exactly this many times (which I've noticed after it was explicitely pointed out by a speaker).
	So the thing is that at least I don't even notice that from going on. According to Michael repeating words like this shows you're listening (and caring) to the other person.

### Domain-Driven Design: Hidden Lessons from the Big Blue Book, Nick Tune

I admit I've read this book many years ago and more or less completely forgot about it. I guess it was way before my time since I wasn't even a junior back then.

Advice:
1. Event storming is a technique that allows non-techies to equally participate in modelling the domain. I'm definitely going to try this out on unsuspecting teammates.
	I find that the more the domain is complex the larger semantic gap becomes, which eventually leads to conflicts, misunderstandings, mistakes and delay so having some tools to ameliorate the gap would be really helpful.
2. There is an [awesome-eventstorming](https://github.com/mariuszgil/awesome-eventstorming) list of suggested practices.
3. The big blue book is a book of heuristics. There is not silver bullet (still)
4. Bounded context basically implies the team, that is behind it. Even if other teams don't want to change the domain to clarify responsibilities it's still possible for one team to go all-out and start the propert transition.

### Building and Scaling High Performing Technology Organizations, Jez Humble

Takeaways:
1. The majority of features delivers 0 value (tested at Amazon)
2. Metrics that are best to observe are:
	- deploy frequency
	- lead time to change
	- change fail rate
	- time to restore service
3. Read the book: Accelerate DevOps
4. A distinction should be made between monitoring and observability.
5. If Q/A writes tests that statistically doesn't affect delivery. They will be unhappy about this when I tell them.
6. Westrum typology to measure culture - this is the reason why conferences are awesome. I need to dig deeper into DevOps at another opportunity.
7. Using displays (for effective work-in-progress) statistically affects performance

### Unit Tests as Specifications, David Bernstein

I'm mentioning this talk because I attended it but was somewhat dissatisfied with it. The only takeaway for me is the following:
Quote: 'Test that never fails is a lie'
I guess that makes me quite the politician. But in retrospective I find it quite true.

### Breaking Codes, Building Jets, and Designing Teams, Randy Shoup

This was a really awesome talk. I've felt for a long time that agile wasn't really the innovation. And this talk basically shows on examples
that it's all been done before at Bletchey parc(Enigma and Loreny ciphers), Skunk Works(Stealth technology), Xerox PARC(WYSIWYG, SmallTalk, GUI, laser printers).

At Bletchey parc they employed a today unimaginable amount of women *75%* . I guess we really failed as an industry with regards to that.
They also employed native indians and in general had a lot of diversity in their teams. I really like the fact that at conferences organisers started
to think and push diversity tickets. Still the industry feels as homogenous as it can be today.

I recall that at Skunk Works there was a rule that engineers always had to be close to the actual hardware being built.

At Xerox PARC I recall engineers were free to propose and gather partisans for their own ideas. Bad ideas would eventually wither and die while good ones would lead on to become what we still use every day.

I guess I don't really know all that much about computing/organizational history. Buzzwords keep popping up for concepts that I eventually find to be yesterdays news.

### Actionable insight with derived second order monitoring data, Jeremy Edberg

This was my favorite tech talk of the conference. Lots of stuff to put on my TODO list:
1. Use serverless for own code and docker for others. 
2. Double exponential smoothing (Atlas)

	For jagged timeseries basically apply a smoothing function to get nicer curves which can then be fed into a smart algorithm for detecting outages.

3. Bussiness metrics are more important than CPU use.
4. If an alert is fired once and never again that likely means it's a random encounter. Alerts should be put on failure rate.
5. t-digest (Elastic) - this was briefly mentioned but goes on my TODO list
6. Cumulative flow diagram (for queues show consumption and generation of messages - to find patterns where consumption severly falls due to failures or other reasons)
7. Rendez-Vous caching 

	I knew what hotspots are but haven't seen a nice existing hash function that avoids hotspotting. Basically when a request hits a distributed system (load balancer or queue)
	hashes get used to select which process/machine gets to process it to nicely evenly distribute processing of requests.

8. Using 2nd order (think movement, speed, acceleration(2nd derivative by time)) metrics has a lot of added value for monitoring systems.

### Unlearning - The Challenge of Change, Jessie Shternshus

I recall an anecdote of how a revers bike was built and nobody was able to ride it. Eventually a kid figured it out.
The idea is that our knowledge eventually impeeds us and figuring out how to forget can benefit me.

As a developer I'm well versed with forgetting so a bigger issue for me is how to keep important things nice, tidy and accessible.

### SQL Server Performance Tuning Made Easy, Pinal Dave

"Indexes don't improve performance."
I find it obvious why indexes can degrade performance for update,delete,insert statements.
However Pinal showed basically that an index can also kill performance for select statements even if the index is not used at all.
I'm not sure how I feel about this but I'm happy to provoke coworkers with it.

Having more than 5 indexes (give or take) on a table is a sign that things have gone haywire. 

Rebuilding indices is a bad practice mainly because it clears the cache, which immediately creates a performance hit on the database in use.
There are other ways of rebuilding statistics(which I'll need to check on mah ever increasing TODO list).

### A Practical Introduction to Coaching (hands-on session), Heidi Helfand

Heidi made us go into a circle and practice head first coaching(co-active coaching). All-and-all it was awkward and somewhat rewarding.

Some basics of coaching:
	- listen to what the other person is saying (not yourself)
	- mirror the other person 
	- repeat and/or paraphrase them (so they know you're paying attention)
	- use powerfull open-ended WHAT questions to guide conversation

It looked easy at first but I found it was quite difficult to put it all together.

Some takeaways:
	- coaching is a way of helping a person/team/org move from point A forward
	- coaching is not therapy, if things get personal it's better to refere the person coached to a specialist that can deal with that
	- coaching is not counseling or mentorship(giving an opinion, advice, argumented study) - you want to help the person coached help themselves (because the coach doesn't really know where they want to go) 
	- a typical coaching session may look like this: let the person coached vent, ask them what problem they want to solve, use techniques mentioned to help them solve their own problems and end by taking some accountabiliy(like call me when done with what you intended to do by some time)

### Dev and Test Agility for your Database with Docker, Julie Lerman

I went to the talk even though I've done this before but from my experience digging into something really basic like for-loops sometimes yields some surprising my-life-was-a-lie moments.
It was nice to hear a presenter show something that I've already done in its entirety. It show that even when dealing with hard legacy it's still possible to be at the bleeding edge at times.

### Rethinking Identity with Clojure, David Nolen

David basically made a bit of an elevator pitch for Vouch but it's a really cool thingy. It allows for passwordless logins using your phone and
is an alternative to various 2FA, MFA schemes. The underlying idea is that by separating data and code it's possible to create simpler, easier to manage systems.
A correlation was made to how we all login today (email, password) and leave the user to either use a password manager (and put the master password on a stick-it)
or just put everythin on stick-it notes, or basically just use weak, easy to remember passwords.

The idea is that we can eventually ditch the password field. The thing is that everywhere where MFA is used, I also always encounter the password.
So if the password was ditched in favour of a HW key this idea would be great. If not however this just basically even further complicates the system.
