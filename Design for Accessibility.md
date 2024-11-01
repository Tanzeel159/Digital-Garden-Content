---
tags:
  - Inbox
Status: Seedlings
Related: 
owner: Tanzeel159
repo: Digital-Garden-content
attachment: true
dataview: true
share: true
date created: 2024-03-27 01:48:29
date modified: 2024-10-31 08:51:38
---
## Notes

### Web Accessibility 

- People with disabilities can equally perceive, understand, navigate and interact with websites and tools. They can equally contribute without barriers
- Digital products (web apps, mobile apps, software, wearable tech, extended reality experiences (AR/VR), voice-touch experiences )
- Usability for all
- Accessibility /= boring designs. It enforces constraints to develop better products for all users.
- Disabilities

| Permanent                   | Temporary            | Situational                                                  |
| --------------------------- | -------------------- | ------------------------------------------------------------ |
| born with vision impairment | glasses prescription | being in bright sunlight not able to see your phone properly |
### Usability 

- user friendly, intuitive, efficient, free of frustrations , aesthetic , modern looking , cohesive
- usability alone doesn't make it accessible to others

## Accessibility 101
### Who is Accessibility about ?

- we should think of designing for people rather than passing certain automated tests or to meet any legal project requirements . 
- think about people and their situations.
- Ex - If I was a person with low vision or color blindness, what would I need to understand what the hover state was conveying to me, or the focus state, or the selected state.
- Different assistive technologies : 
	- Alternative web browsers
	- Braille for the web
	- Eye-tracking software
    - Head wands
    - Mouth sticks
    - Screen magnifiers
    - Screen readers

### Number of people accessibility includes

> [!important] 
>  **Designing with accessibility in mind makes interfaces and experiences more usable for everyone – _even those without a disability._**

- **Screen reader** isn't just for blind people . Helps others including people with eye fatigue, learning or cognitive disabilities, helps in multitasking for others in general.
- **Closed captions** aren't just for people who have hearing impairment but come in handy when we don't have earphones , or for people who struggle to understand the language 
- More than 1 billion people have some kind of disability . They rely on accessibility 
- 5 main categories of disabilities

| Visual                                       | Motor                     | Auditory           | Speech                   | Cognitive                             |
| -------------------------------------------- | ------------------------- | ------------------ | ------------------------ | ------------------------------------- |
| includes people with photosensitive epilepsy | physical and neurological | related to hearing | related to voice, tongue | cognitive ability - understanding etc |

### Pro tips

1) Accessibility is for some, useful for all
2) Think it in terms of addressing people's concern and not to fulfil some standard, checklist (Ex - Button hover state implementation instead of thinking it as implementing by going through a rulebook, think of real world cases where you want the user to immediately identify it and proceed accordingly )
3) Designing for accessibility is not designing for edge cases (if we think of implementing for regular users and then consider people with disabilities as edge cases , then our thinking is flawed) - reinforces [social exclusion](social%20exclusion.md) and [marginalization](marginalization.md).
4) Accessibility should by default be considered in definition of usability . Designing for accessibility, means our products will come out with a higher level of usability, a better UX, and greater customer satisfaction.

### Accessibility Myths

1) User don't complain about accessibility so we are doing okay .  (only 10% users report about accessibility)
2) Fixing accessibility is expensive . (retrofitting projects with accessibility will be expensive . better to plan and )
3) accessibility isn't my job . (making product accessible to all users is a big goal )
4) market too small to justify the effort (market is significant)
5) accessible design is boring design (embracing accessibility can open up invention , should work for those in need and be invisible to those who don't need it)

### Business case for accessibility 

1) Drive innovation . ~ accessibility problems are mainstream breakthroughs for tomorrow.
2) Minimize legal risk . ~ countries have laws requiring digital accessibility and lawsuits against those who don't follow.
3) Enhance brand reputation . ~ can influence and increase your reach . 
4) Extend market reach .  ~ increases the reach since spending power of people with disabilities is huge.
5) Improve SEO

### Guidelines to keep track of

1) **WCAG** - Web Content Accessibility Guidelines
2) **ADA** - Americans with Disabilities Act
3) EU 301 549 - EU Web Accessibility Directive

### Who is responsible for ensuring accessibility ?

1) **Organization leaders**
2) **UX Designer/ Developers** - responsible for conducting user research and usability testing that **includes people with disabilities**. These include :
	- the user & business needs assessment, 
	- the information architectures, 
	- the wireframes, 
	- the interaction designs, 
	- the mock-ups or the prototype,
	- the design system, and 
	- anything else we put out. It all needs to be designed for accessibility. 
3) **content writers and editors** -  responsible for devising an accessible content strategy and accessible content structure.
4) **in-house or third party accessibility expert** - completes an accessibility review of the prototype/mock-ups before they go to development.
5) **developers** - they must comply with the latest version of the WCAG Level AA in all the code they write.

### Test for accessibility 

1) **Manual Testing** - Manual testing is when a human goes through each interface one by one and looks and tests for accessibility issues.
	- Easy to do
	- possible to do at any stage
	- cheap
	- allows us to be more thorough
1) **Usability Testing** - different users (multiple races, genders, ages , people with disabilities) test our digital product and share their thoughts . (test group should be diverse and inclusive)
2) **Automated Testing** - using automated tools to test accessibility , can be on website we are redesigning to get baseline metrics or on test website where code is developed.

### What does accessibility expert do ?

- Must know about WCAG and accessibility practice in depth.
- They will test each component shown on the web page to see that it works accessibly, and check the page in different states, such as at high zoom levels (up to 400% and higher), and using high contrast modes.
- They will use screen readers (JAWS and NVDA are the two readers most used by blind people).
- They will do testing on at least mobile devices including Apple iPhones and/or iPads, and Android phones and tablets
- They will use specialized accessibility manual test tools such as a colour contrast tool.
- They will look at all of the mark-up to check for known potential issues, and will also check all of the images for correct alternative (alt) texts.

### Top tools

1) WAVE Tools ([WAVE Web Accessibility Evaluation Tools](https://wave.webaim.org/))
2) NoCoffee ([NoCoffee – Get this Extension for 🦊 Firefox (en-US)](https://addons.mozilla.org/en-US/firefox/addon/nocoffee/))
3) Axe ([axe DevTools - Web Accessibility Testing](https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US))
4) Enterprise ([Browser extensions](https://www.siteimprove.com/integrations/browser-extensions/))
5) ANDI ([ANDI - Accessibility Testing Tool - Install](https://www.ssa.gov/accessibility/andi/help/install.html))
6) Figma Plugins ([Tackle accessibility in your designs with these useful plugins | Figma Blog](https://www.figma.com/blog/design-for-everyone-with-these-accessibility-focused-plugins/))

---
## Related

1) [Design](Design.md)
2) [Color Contrast](./Color%20Contrast.md)
3) [Color Independence](Color%20Independence.md)
4) [Wording Interactive Elements](Wording%20Interactive%20Elements.md)
5) [Styling Interactive Elements](Styling%20Interactive%20Elements.md)
6) [Designing Interactive Elements](Designing%20Interactive%20Elements.md)


---
## References

1) [Stephen Murray and his Tobii PCEye Go - Focus on the Game - YouTube](https://youtu.be/2zh2UMK8xf0)
2) [How A Screen Reader User Surfs The Web - YouTube](https://www.youtube.com/watch?v=OUDV1gqs9GA&feature=youtu.be)
3) [Site Unreachable](https://www.respectability.org/2018/12/short-film-about-playground-inclusion-wins-international-acclaim/)
4) [Incredible Ageing Suit | Horizons - Virtual Old Age | BBC Studios - YouTube](https://youtu.be/PXLVLSgX3Ig)
5) [Misconceptions About Blindness! (disability misconceptions tag) - YouTube](https://www.youtube.com/watch?v=kYp55K0TUYQ)
6) [To Care & Comply: Accessibility of Online Course Content - YouTube](https://www.youtube.com/watch?v=eks3r-nE9lU)
7) [ROCKYNOHANDS | PUBG WITH NO HANDS - YouTube](https://www.youtube.com/watch?v=hJCHRPzRI94)
8) [Job Accommodations to My Computer | Proloquo2Go | Self-Determination | Wisconsin BPDD - YouTube](https://www.youtube.com/watch?v=uMG2byjDQL8)
9) [Meet Elle - National Parent Center on Transition and Employment](https://www.pacer.org/transition/video/player.asp?video=32)
10) [Institutionnel : Diversité | INA](https://www.ina.fr/video/PUB2867758021/institutionnel-diversite-video.html)
11) [Barclays | Busting Accessibility Myths - YouTube](https://youtu.be/_1yGFn7OIDY?si=PHSuF_Cp5meY_SG-)
12) [Section 508 Compliance & Web Accessibility - TPGi](https://www.tpgi.com/508-compliance/)
13) [Universal Design and Accessibility | Section508.gov](https://www.section508.gov/develop/universal-design/)
14) [ANDI Introduction - YouTube](https://www.youtube.com/watch?v=BpBtwsxg-k4)
15) [Redirecting…](https://www.section508.gov/test/web-software/andi-training-videos)
16) [How do I test my website for accessibility? - YouTube](https://www.youtube.com/watch?v=hV24ZhPgbtM&feature=youtu.be)
17) [Are automatic accessibility test tools any good?](https://www.linkedin.com/pulse/automatic-accessibility-test-tools-any-good-guy-hickling/)