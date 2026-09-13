[r/bugbounty](https://www.reddit.com/r/bugbounty/)•27d ago

[Interesting-Disk-408](https://www.reddit.com/user/Interesting-Disk-408/)

Hunter

# Am I wasting too much time on bug bounty?

[

Question / Discussion

](https://www.reddit.com/r/bugbounty/?f=flair_name%3A%22Question%20%2F%20Discussion%22)

I need to talk to some experienced bug bounty hunters because I’m honestly starting to get frustrated

Lately, I’ve been spending a lot of time hunting, doing recon, testing endpoints, trying different attack surfaces, etc. But when I finally submit reports, a lot of them end up being marked as **Duplicate**.

And I’m not talking about one or two reports. I’ve had a bunch of them end up this way.

At this point I’m starting to wonder if I’m approaching bug bounty the wrong way.

I understand that duplicates are completely normal and that someone else may have found the same issue before me. But when you spend hours investigating something, write the report, and then get "Duplicate", it can feel like you’re just burning time.

For those of you who have been doing bug bounty for a while:

- How do you reduce the number of duplicates you get?
    
- Do you prioritize newer features/attack surfaces?
    
- How much time do you normally spend on a finding before deciding it’s probably not worth pursuing?
    
- Do you have a specific methodology for finding bugs that are less likely to already be reported?
    
- And honestly, how many duplicates did you get when you were starting out?
    

I’m not looking for shortcuts or a magic tool. I’m trying to understand how experienced hunters decide **where to spend their time**.

Would appreciate any advice or even stories from people who went through the same phase.

[latnGemin616](https://www.reddit.com/user/latnGemin616/)

•[27d ago](https://www.reddit.com/r/bugbounty/comments/1vnch6i/comment/p3gcdpf/)

_sigh .. another Duplicate rant_

OP -

_The Good News_: Duplicates means you're doing something right. The problem is you are the 250th person that has done it, and there have been many others that came before you.

_The Bad News_: BBH is super-saturated with newbs who have been sold a lie that hacking is the way to prosperity. I don't know what goes on in SE Asia and parts North, but its gotten really bad.

_The Ugly News:_ AI has produced a crap ton of AI slop by script-kiddies who don't know the effort of pen testing, so they gum up the program with junk AI reports that are overwhelming the triage process.

_The Recommendation:_ Quit whining about duplicates. Pick a program that has minimal amount of reporting in the target. Or choose an aspect of the program that no one has touched. I can promise you, there will be a ton of people who know web, but hardly anyone goes for API or mobile.

[ibackstrom](https://www.reddit.com/user/ibackstrom/)

•[27d ago](https://www.reddit.com/r/bugbounty/comments/1vnch6i/comment/p3gzev7/)

_Pick a program that has minimal amount of reporting in the target_

everybody is taking this programs nowadays lol

[YouRSav1ouR](https://www.reddit.com/user/YouRSav1ouR/)

•[7d ago](https://www.reddit.com/r/bugbounty/comments/1vnch6i/comment/p7ggahf/)

When you say API isn’t that part of web?

[SilentRoberto](https://www.reddit.com/user/SilentRoberto/)

•[27d ago](https://www.reddit.com/r/bugbounty/comments/1vnch6i/comment/p3gdp9r/)

I think it boils down to luck. Personally I only started enjoying the finesse of complex clientside exploitation later and never even bothered getting into the nuclei scanning stuff. All the XSS I reported were duplicates.

I got rewarded over a hundred bugs across platforms and whenever I would log high impact bugs they never turned out to be duplicated except for a few sensitive disclosures that I didn't exploit further.

My advice is to focus on high impact bugs, they are less likely to leave critical shit around so it won't get you depressed as often.

Also, honor the joys from the small bugs. Don't be a fool and report small nuggets of info. Try to escalate as often as you see something new. Whenever I found an IDOR there was often a case I could find more things by virtue of this. Same with seemingly unexploitable exceptions or debug statements.