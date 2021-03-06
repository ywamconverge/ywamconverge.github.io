CAUTION: This document is under constant draft change at the moment.

This is a hands-on tutorial that volunteer software developers reference to get setup in order to make contributions in a collaborative way. This was written to ensure that you (a developer/graphic artist, etc.) get <strong>trained</strong> on a professional approach to software development while improving the non-profit's digital assets. The sections here are:

A. <a href="#Understand">      Understand the mission</a> (the organization and yours)<br />
B. <a href="#TechArchitecture">Understand the technical architecture</a><br />
C. <a href="#PickProject">     Pick a project</a><br />
D. <a href="#Collaboration">   Setup collaboration tools and techniques</a><br />
E. <a href="#Website">         Copy the public-facing website</a><br />

F. <a href="#NewSandbox">      Create a new Salesforce sandbox</a> ("Dev03") with metadata<br />
G. <a href="#SalesforceData">  Import object data into Salesforce sandbox</a><br />

H. <a href="#Changes">         Plan changes, update test scripts</a><br />
I. <a href="#TestDeploy">      Run tests, make changes, and deploy</a>

<hr />

<a name="Understand"></a>

## A) Understand the mission

   <a name="Persona"></a>
   
   For this non-profit, the <strong>persona</strong> are: interns, hosts, mentors, donors. 
   Each person goes through different status over time: prospective, active, inactive, alum.

1. Obtain a coupon from John to access the video courseware.
1. This is a free 48-VIP Backstage Pass to <a target="_blank" href="https://ywam-converge.teachable.com/purchase?product_id=2605714">Converge Course</a>.

   The course material was migrated from <a target="_blank" href="https://coursesites.com/?sig=Mwuk9E96d1zi4kLs58vOveO3Tl8=&courseId=_190749_1&timestamp=1549132709&inviteId=BB?BB_QzCGaVfkHcOjnCyDupFaIrNNbv5DmyN82PEvwEmTOMMtUG+4ivX5IA==#invitation-student">the Blackboard system</a>. 
   accessed <a target="_blank" href="https://blackboard.coursesites.com/ultra/courses/_190749_1/cl/outline">here</a>)
 
3. To understand the Youth With A Mission movement, YWAM Converge is part of, go to <a target="_blank" href-"https://ywam.org/about-us/values/">YWAM Values</a>.
4. Click "Go to Course Curriculum" and start with the "Welcome to Converge" unit.
5. Scroll down to watch the "What is YWAM" video. <strong>Click the volume icon to unmute.</strong>

   When did YWAM (the parent organization) start? See <a target="_blank" href="https://youtu.be/Uz0EesM-G04">https://youtu.be/Uz0EesM-G04</a>

6. Scroll down the page to see the diagram summarizing the activities by phase:

   <img alt="ywam-contribute-648x636-38472.jpg" width="500" src="https://user-images.githubusercontent.com/300046/54088143-34372b00-4331-11e9-952c-c7470f39d708.jpg">

7. Open a browser tab to the <a target="_blank" href="https://ywamconverge.org/faq/">FAQ</a> (Frequently Asked Questions) to see if you can answer the questions before revealing the answer. Kinda like a quiz.

   <a name="Procedures"></a>
   
   ### Process/Procedures

8. Watch demo video of <a target="_blank" href="https://www.youtube.com/watch?v=jQuuvYIbbTA&feature=youtu.be">How to apply for a Converge intership</a> [2:20] No sound. The Ruby system is not mobile-friendly (progressive), addressed by <a href="#ResponsivenessUpdates">the changes for Progressive mobile use below</a>.

9. Watch demo video of <a target="_blank" href="https://youtu.be/ejz9HEbg9Xo">host app</a> (No sound) at 
   https://www.youtube.com/watch?v=hSqbotfxZAA Dec 23, 2015

9. Watch "Create an Internship" Host App help videos: (These are to be added to the top of the Create and Internship app pages as thumbnail videos and links to youtube where translated CC: will be available.)
 	Page One: https://youtu.be/Y8b8EjnE6p8
	Page Two: https://youtu.be/VF6HuSuJXdo
	Page Three: https://youtu.be/hGm5-ETqpaI
	Page Four: https://youtu.be/IrdopkSjueM
	Final Page: https://youtu.be/K3iDVedxYnU

<a name="TechArchitecture"></a>

## B) Understand the technical architecture

The system consists of several components, <a target="_blank" href="https://docs.google.com/presentation/d/1o_T8XRfeiDLD62ums2hHYid5_qIFNHUlAkQ3YtV6E1k/edit#slide=id.p">described by this system flow chart on Google (created using Lucid Chart)<img align="right" alt="ywan-architecutre-2019a-200x183-7427" width="200" src="https://user-images.githubusercontent.com/300046/53695300-b2bb2800-3d87-11e9-9b8e-759a92d654dd.jpg"></a>

   *<a href="#UserStories">See PDFs of User Stories for Hosts, Mentors, Students, and Donors</a> information used internally to build UX. <a target="_blank" href="https://www.dropbox.com/sh/nr245gp42boee6w/AADRuqGLNvIjqrG1XPT3Ve9ya?dl=0">User Stories</a>
   * <a href="#TrainingSite">A training management website</a> used by interns to learn about being an intern. Videos on it are stored (as Public) on the <a target="_blank" href="https://www.youtube.com/channel/UCacj____6p8-iiIN_Nk-iBw">YouTube channel</a>
   * <a href="#Website">A public-facing website</a> that exchanges information dynamically with
   * <a href="#Salesforce">A Salesforce org</a> database used internally for administration.

   * <a target="_blank" href="https://www.youtube.com/watch?v=FwNdD0yrBE4&list=PLJY5a7HPiwbWpw63i-4sFoKfXvEe-zxBV">Audio podcasts from 2018</a> are also stored on YouTube.
   * <a target="_blank" href="https://podcasts.apple.com/us/podcast/converge-stories-podcast/id1440794904/">Apple podcasts</a>
   * <a target="_blank" href="https://www.facebook.com/YWAMOCNJ/">Facebook</a>
   * <a target="_blank" href="https://www.instagram.com/ywamconverge/">Instagram</a>

<a name="PickProject"></a>

## C) Pick a project

Some volunteer opportunities are listed in <a target="_blank" href="https://rwjf.catchafire.org/volunteer/?name_filter=ywam%20converge&page=1">CatchAFire.org</a> managed by admins using the <a target="_blank" href="https://rwjf.catchafire.org/dashboard"> dahboard</a>.

a. Team: How to get more people to be aware of this (advanced training to make a difference)? What are the outlets?
   
b. John: Create videos for display in emails (instead of text) about next steps, etc. within a drip email sequence.
   
c. Mike Ko: Create <strong>automated test scripts</strong> to verify whether the system works "end-to-end" (for different personas), to identify whether the sytem still works after changes.

   1. Instructions for installing https://www.cypress.io/ on Windows (not Mac yet) in https://github.com/ywamconverge/ywamconverge.github.io/edit/master/TESTING.md and opinions about it vs. other tools
   2. Write tests to invoke then assert responses from top menu (Facebook, Search for "signup", Donate, Videos on landing page) on the production page https://www.ywamconverge.org/.
   3. Student sign-up (not appearing in prod but in test site)
   4. Track over time how long it took to load page.
   5. other use cases (pages).

   <a name="ResponsivenessUpdates"></a>
d. Implement CSS/HTML changes to media query, etc. to display mobile screen size, as designed by Mona at:
   https://docs.google.com/document/d/1fzrrrBXYAxcYfSFz-zeX42KR2iPnJzuB73LpvWk8EqY/edit

d. Upgrade front-end server version upgrade (to Ruby, Postgres, TLS 1.2 for Braintree, etc.).
   
e. Wilson: Create instructions (this page) to enable volunteers to create a dev environment and contribute changes. 
   
f. Dan/Wilson: Convert bash scripts and instructions to create a dev instance of Ruby server running on Ubuntu.
   
g. Kermit: To <strong>troubleshoot without worry</strong>, define manual procedures and scripts to create a <strong>stand-alone Saleforce Dev. instance</strong> (a "crash dummy") containing metadata and filtered/cleansed data from production org sandbox:

   ### &nbsp; &nbsp; &nbsp; Administrator:

   1. Configure templates and <a target="_blank" href="https://help.salesforce.com/articleView?id=data_sandbox_create.htm&type=5">generate a Dev. sandbox</a> from prod instance.
   2. Create test scripts on sandbox so running it doesn't corrupt or degrade the production instance.
   3. Export metadata (coding) from Sandbox.
   4. Create data extract from Sandbox.
   5. <strong>Cleanse data</strong> 
   6. generate additional test/mock data using <a target="_blank" href="http://mockaroo.com">mockaroo.com</a> (generates up to 1,000 rows free).
   7. Copy cleansed data into a location available to developers.
   <br /><br />

   ### &nbsp; &nbsp; &nbsp; Developer (volunteer):

   1. Import metadata (coding) into Dev. instance.
   8. <a target="_blank" href="http://pages.mail.salesforce.com/gettingstarted/sales-cloud/import-export-data/">Import</a> cleansed data into Dev using DataLoader.
   9. Modify test scripts to run on imported Dev. instance.
   <br /><br />
   
h. Enable and test disaster recovery.

i. <a target="_blank" href="https://www.catchafire.org/volunteer/26956/ywam-converge-in-ocean-city--nj--tech-systems/">PROJECT:</a> To best communicate with student/interns, we need someone to research, propose, and then develop the best option for texting internationally to students, hosts, mentors, donors. Wilson said he and Kermit saw a company offering a good texting solution at Dreamforce. Texts can replace emails if they include links to static web pages or links with reminders to log in to dashboard to complete an activity.  

j. Make <strong>introduction videos</strong> to each of the <a href="#persona">persona</a> for display on the website and to make emails more "alive".

k. Create training for mentors ?

l. <strong>Translations</strong> of the site into various languages. We have a team currently translating the site into Spanish. A LOT of their work is already done. At some point, I want to get a Volunteer Project posted to insert the “es:” text into the code. (BTW, all the training videos are also being translated to Spanish to be inserted into the videos too. That will be another project. The team in Colombia is translating those SRT files now.)
   
m. Architect a more secure way to maintain passwords and other secrets for team (Hashicorp Vault, etc.)
   
n. Propose one of your own. 

Cloud Recording of meeting discussing the following: https://zoom.us/rec/share/xcB6Jpfb51JJYomUtHPHcKNxG4X9eaa8h3BKqaFcyU8YjDv6Xi41Tiu0DZIuNqEF
	
	1. Create annimated video instructions for Host and Student applications
	2. Update Ruby Refinery
	3. Reset Footer links to refinery pages
	4. Make CSS changes for Mobile Responsiveness -  https://docs.google.com/document/d/1fzrrrBXYAxcYfSFz-zeX42KR2iPnJzuB73LpvWk8EqY/edit
	5. Make Task Flow corrections - https://projects.invisionapp.com/share/CVUUOL59XU4#/screens/393555053/comments/125810009

	6. Add links to Udemy Course on Rails site.
	7. Internationalization - https://www.refinerycms.com/guides/translate-refinery
		a. Translate to Portugues
		b. Translate to Korean
		c. Upload and manage all internationalization files
	
	Additional Items Kermit is working on:
	8. Test Communities in Salesforce
	9. Integrate Communities in Rails site.

<a name="Collaboration"></a>

## D) Setup Collaboration

If you haven't used the tools mentioned here, we will train you so that you can contribute confidently.

1. Make an appointment with John at
https://calendly.com/john-t-henry

   John makes use of Zoom for group video conferencing that can be recorded. John Henry is inviting you to a scheduled Zoom meeting.

https://zoom.us/j/6212275173?pwd=N01vS1FoUS9qR2thbzdLb2J4c0FWQT09

2. From John, get an email invite to the Slack channel used by developers (join the channels):

   <a target="_blank" href="http://ywamconverge.slack.com/">http://ywamconverge.slack.com</a>

   Click the "Channels" heading on the left pane.
   Click on a channel name. Click on "Join Channel".

3. Use your email to get a free GitHub account and let us know what your GitHub account name is. Then you can fork our GitHub to your own account. Create a branch under your account to make changes, then create a Pull/Merge Request. 

4. We share sensitive info like passwords only on WhatsApp chat.

5. Saleforce Chatter real-time text message we use to make announcements that get sent out as emails.

6. WhatsApp group.

7. Get AWS account credentials from one of the admins.
8. After logging in the first time, you are prompted by AWS to change the password.

<a name="ywamconverge"></a>

### D1) ywamconverge.org public-facing app 

To work on the site:

3. Use the Cloud9 app in the us-east-2 (Ohio) region:

   <a target="_blank" href="https://us-east-2.console.aws.amazon.com/cloud9/ide/231f5912a5af454aa264f17f2cc81c68">https://us-east-2.console.aws.amazon.com/cloud9/ide/231f5912a5af454aa264f17f2cc81c68</a>

4. There are different environments (including a "Translator environmet").

   ![ywam-c9-top](https://user-images.githubusercontent.com/300046/75109815-2e476200-55f5-11ea-9c96-3515706546e7.png)

   "Translator Environment" files are used in<br />
   <a target="_blank" href="https://glenis.ywamconverge.org/">https://glenis.ywamconverge.org</a>

   Changes in one enviornment are copied to others by admins.

   <a name="localization"></a>

5. Localization resource yaml files are within folder <strong>config/locales</strong>

   ![ywam-c9-config](https://user-images.githubusercontent.com/300046/75109920-ac0b6d80-55f5-11ea-82f9-4e43e6bf12fa.png)

   * en.yml is for english.
   * es.yml is for spanish.
   * ko.yml is for korean.
   * These are <a target="_blank" href="https://www.loc.gov/standards/iso639-2/php/code_list.php">legacy 2-letter ISO 639‑1 codes</a> rather than the <a target="_blank" href="https://en.wikipedia.org/wiki/Language_code">more modern 3-letter codes</a>.
   <br /><br />

   Text "hard-coded" in app code lookup keys when displaying text.

   <pre>internship_location_culture_heading: "Internship Location & Culture"</pre>

   in en.yml in es.yml is:
   
   <pre>internship_location_culture_heading: "Lugar & Cultura de Pasantía"</pre>

   PROTIP: When beginning to translate an additonal language, copy the en.yml file, and do a find/replace all of <tt>: "</tt> to <tt>: "#</tt> so that a <tt>#</tt> leads each English sentence so that it's easier to recognize untranslated text.

   Remember that each new key needs to be added to every yml file.

6. App code is mostly in folder <strong>app/views</strong>

   Specifically: app/views/projects/show.html.haml

   Coding of a key which the program will replace with text looked up from a resource file:

   <pre>%h3= t(:internship_location_culture_heading)</pre>

   NOTE: Modern English language does not have some subtlies in other languages.
   Many commercial apps contain additional coding for differences in formal vs informal (slang) language. Sophisticated apps may show different words if the person is a male/female, or to show respect to a senior person, etc. 

   WARNING: Not all English words should be replaced with translation keys.
   Some code reference programming text, such as:
   
   <tt>%p= @p.team_mode ? "Team" : "Individual"</tt>
   
   and
   
   <tt>class: "button button-orange entypo-apply"</tt>

<a name="Website"></a>

## E) Copy the public-facing website

1. Open an internet browser to visit the production webpage:

   <a target="_blank" href="https://ywamconverge.org/">https://www.ywamconverge.org/</a><br />
   YWAM Converge - Ocean City New Jersey

   The tech behind the website consists of several components (all free open-source):

   * Ubuntu 18 operating system (contains ssh and yum package manager)
   * Utility Git (needed by Capistrano)
   * PostgreSQL database
   * Ruby (programming language interpreter)
   * Rails engine <a target="_blank" href="https://www.refinerycms.com/">Refinery CMS</a> (4.0.3 from the Gemfile). It supports Amazon S3 cloud storage and makes use of ...
   * ElasticSearch to do indexing and
   * Dragonfly for image editing

   * Redis database to manage queues to Salesforce
   * Sidekiq to proxy and manage Redis
   * NGINX ?
   * TODO: Utility to backup database
   * TODO: Utility to cleanse data
   <br /><br />

2. Code and documentation about the website is at this private GitHub repository:

   <a target="_blank" href="https://github.com/wilsonmar/ipo-web">https://github.com/wilsonmar/ipo-web</a>

   It was previously at: https://github.com/ipoconnection/ipo-web

   BTW The name "IPO" is a carry-over of previous branding, and kinda stuck. We should rename it someday.

   If you have access to examine the repo off-line, on your machine, create a folder and clone the repo onto your local laptop.

3. Click the "Branch: master" and select the branch Dan is current using: <tt>upgrade-rails-4.0</tt>

   That branch name will be different in the future.

   <tt>README.md</tt> describes each component and installation process in more detail.

   <tt>README.rdoc</tt> contains instructions for running on an Appl MacOS laptop. 
   But since the system runs under Ubuntu in production, we are converting scripts and instructions to that OS, and assume that you are using a Docker or cloud image (running on Amazon Lightsail</a>, etc.).

4. Create a VPC instance within <a target="_blank" href="https://wilsonmar.github.io/lightsail">Amazon Lightsail</a> or other bare-bones VPS (Virtual Private Server). 

   PROTP: Begin with the 512 MB RAM to practice loading, then move up as necessary.

   TODO: In the future we will define files to use Docker with Kubernetes.  

5. Open an SSH session to your machine and login using the <strong>default user</strong> ("ubuntu").
6. Create another user, <strong>deployer</strong>.

	<pre>sudo adduser deployer --ingroup admin
	</pre>

1. Type in password when prompted with "Enter new UNIX password:".

   <pre>
passwd: password updated successfully
Changing the user information for deployer
Enter the new value, or press ENTER for the default
Full Name []: 
Room Number []: 
Work Phone []: 
Home Phone []: 
Other []: 
Is the information correct? [Y/n] 
   </pre>

7. Reboot and login as deployer to run the Bash script which installs software, configure it, and populate the database, and runs a smoke test to verify viability.

8. Copy the command to invoke the install script to your Clipboard (by triple-clicking this line before pressing command+C) this string:

   <pre><strong>bash -c "$(curl -fsSL https://raw.githubusercontent.com/wilsonmar/DevSecOps/master/Ruby/ywam-setup-all.sh)"</strong></pre>

1. Get on your VPC command line interface and press command+V to paste the command.

   On Amazon Lightsail, you would need to first click on the orange clipboard icon, then paste in its form, then click on the CLI (black screen), then right-click to paste (on a Mac, press two fingers at once on the touchpad). Press Enter to run the command.

   BTW The script is supposed to be idempotent because it erases resident folders from the previous run.


<a name="NewSandbox"></a>

## F) Create a new Salesforce sandbox with metadata

1. Get an account name to the Salesforce org you want to work on (in an email).
1. Login as admin. into the Production org (which has the data)?
1. Get into Setup. 0:53

1. Search “Sandboxes”. 1:05

   Note the number of each type of sandbox available. 1:21

   <a target="_blank" href="https://user-images.githubusercontent.com/300046/62666711-bd36aa80-b941-11e9-8e65-ca2f48f370a1.png"><img alt="sf-ywam-sandbox-list.jpg" src="https://user-images.githubusercontent.com/300046/62666711-bd36aa80-b941-11e9-8e65-ca2f48f370a1.png"></a>

1. Click “New Sandbox”. 3:05 
1. Review the differences among different types of sandboxes.
1. Before typing in the Name field, click “Create From”. 3:32

   <a target="_blank" href="https://user-images.githubusercontent.com/300046/62665843-f2d99480-b93d-11e9-840b-9a987ba83f93.jpg"><img alt="sf-ywam-sandboxes.jpg" src="https://user-images.githubusercontent.com/300046/62665843-f2d99480-b93d-11e9-840b-9a987ba83f93.jpg"></a>

   PROTIP: Because upper-case ones sort to the top while lower-case all appear in the bottom, enforce naming standards. This can confuse sequencing of Dev01, dev02, etc. So do like Salesforce’s “Production” and always use Title capital casing.

1. Click “Next” in the Developer section for Sandbox Options. 4:29
1. Click “Create” without typing anything in the Apex class field.
1. Wait for “Pending in Queue” Status (about 10 minutes), and an email is received 
1. Edit the login URL in the email with subject such as "Sandbox: Dev03 is ready to use".
1. Login using a Username suffixed with the sandbox name and your regular password, such as ".Dev03". Verify your identify.
1. The URL should include "--dev03.lightning.force.com".
1. Active Licensed users would have a Username with the sandbox appended.



<a name="SalesforceData"></a>

## G) Import object data into Salesforce sandbox

Salesforce provides weekly production backup zip. 
It's triggered by a scheduled job from a service account which receives emails when done.
Currently, each backup consists of 330 csv files take 8.3 MB zipped. Unzipped its 107 MB.
The output zip file is copied to an alternative cloud provider (Google Drive) because Salesforce only stores backup files 48 hours, with file name (from a default name such as "WE_00DG0000000ggbAMAQ_1.ZIP") to this example: 

   <tt>ywam-prod-<strong>data</strong>-2019-06-03-3amET.zip</tt>

Metadata (custom fields, reports, list views, workflows, etc.) is extracted to a name such as:

   <tt>ywam-prod-<strong>meta</strong>-2019-06-03-3amET.zip</tt>

TODO: Use UTC.

Due to active changes, <strong>daily</strong> backups are maintained for 13 months (370 zip files).
The assumption is that there is a lot of financial info in the backups.

TODO: Add to the name the number of days since Jan 1 of the year.

3rd party offerings:
* https://skyvia.com/data-integration/salesforce-data-loader
* https://spanning.com/resources/whitepapers/3-ways-to-restore-salesforce-data/
* https://www.cloudally.com/how-to-recover-salesforce-data/
* https://pages.ownbackup.com/salesforce-weekly-export
* https://www.backupify.com/salesforce-backup


### Production security

The production Salesforce instance is <a target="_blank" href="https://studentmobilizationcentre.my.salesforce.com">https://studentmobilizationcentre.my.salesforce.com</a>, but to avoid additional charges we are trying to keep the number of people accessing it. Named users in SF are first initial and last name with no space.

   1. John Henry, as the CEO, owns the all-powerful System Administrator permissions for the production org.
   2. Mary Henry has the System Administrator "Accountant" role.
   3. API IDM is the user for API calls (does not use the UI).
   4. Daniel Bryan is the root System Administrator.

   5. Oliver Tesslof has a System Administrator role. He is a primary Salesforce Dev volunteer
   6. Glenis Acost has a Program Director role as a Spanish Translator.
   7. wilsonmar@uofn.edu
   8. Myriam Parra mision.miriamparra@gmail has a Spanish Approver role.
   <br /><br />

There is a secret repository holding passwords to the production site.

PROPOSAL: Volunteers use generic accounts rather than named ones. For example:

   * admin@ywamconverge.org has the SF Standard "Executive Assistant" role.

   * "tester.312" has permissions to conduct tests and view security settings.

   * "user.415" has permissions to view reports and add opportunities.

   * TODO: Map out users, their roles, and permissions.

### Dataflow diagram

<a href="https://user-images.githubusercontent.com/300046/54088161-85dfb580-4331-11e9-9d10-095f90c4688c.jpg"><img alt="salesforce-contribute-v05-677x301-30618.jpg" src="https://user-images.githubusercontent.com/300046/54088161-85dfb580-4331-11e9-9d10-095f90c4688c.jpg"></a>

The diagram here illustrates, on one page, how the various pieces talk to each other.

Your first exposure to Salesforce is likely the <a target="_blank" href="https://trailhead.salesforce.com/">Salesforce Trailhead website https://trailhead.salesforce.com</a> which provides anyone a free Trailhead account with up to 5 "hands-on org" in a "playground" to use while taking learning modules. The <a target="_blank" href="https://trailhead.salesforce.com/sample-gallery">sample gallery</a> developed by Salesforce Developer Evangelists can be loaded as Dev orgs through the <strong>App Exchange</strong>. Sample packages are "unmanaged" and can be altered when installed. There are also <strong>managed</strong> packages (such as the Non-Profit Success Pack) from Salesforce partners.

Each org (database) contains two types of information: master data values such as customer names and <strong>metadata</strong> (Apex coding, form layouts, and other configurations).

Those who have bought one of the various levels of licenses for production usage have a single PROD org instance. Administrators go into Setup's Sandbox function to create copies of metadata in various types of Sandboxes (abbreviated SBX). Different levels of licenses come with different numbers of each type of sandbox. Dev (Development) Sandboxes are created so developers can add a few records specific to test what they are changing. Other types of Sandboxes contain data copied in. <strong>Dev Pro</strong> Sandboxes have up to 200 MB of test data. <strong>Partial</strong> Sandboxes hold a sampling of data for integration testing.
<strong>Full</strong> Sandboxes contain a complete copy of production records and metadata. 

Since it can take awhile to copy, an email is sent when it's done. To get data records into Sandboxes, we export based on filters in <strong>templates</strong> define within the Salesforce website. The export process also sends an email.

The <strong>DataLoader</strong> utility is used to put data in Sandboxes. Because we are dealing with private production data, <strong>cleansing</strong> for duplicates and/or <strong>masking</strong> for privacy after export needs to done. Doing that directly in production provides for validation before committing. 

Trraditionally, developers create <strong>Change Sets</strong> to patch metadata, and run Salesforce Apex tests and <strong>UI tests using Selenium or TOSCA/Flood.io</strong> before pushing changes through various environments.

In 2018, Salesforce made available DX (Developer Experience) that manages temporary <strong>Scratch</strong> orgs updated by metadata stored in a Git version control repository. Temporary means <strong>7-30</strong> days before they disappear automatically.

To provide <strong>testing scripts</strong> the <strong>test data</strong> they need, <strong>custom scripts</strong> are written to load the test data into Scratch orgs and Playground org. 
QUESTION: Can the DataLoader put custom external test data into the Dev Sandbox?<br />
QUESTION: Can the DataLoader put data into Playground orgs?<br />
QUESTION: Can a custom package be created from a Sandbox?


### Procedures

Each developer makes use of their own Salesforce org to work. This can be a Developer Sandbox provided from the Administrator or a copy of the production Salesforce org. in a Salesforce Trailhead Playground org.

1. At <a target="_blank" href="https://trailhead.salesforce.com/">Salesforce Trailhead website https://trailhead.salesforce.com</a>, sign up for a free Developer org. and sign into it. You may need to first open an <strong>incognito window</strong> to avoid cookies from other Salesforce sessions.
2. <a href="#LoadSF">Load the metadata into your own org.</a>
3. Ask for .csv files containing masked data that has also been cleansed and reduced in size. 
4. Import the test data into your org.
5. <a href="#SFwebsite">Configure the API connection between the website and Salesforce API.</a>


<a name="LoadSF"></a>

### Load metadata into your own org.

@Kermit?

https://developer.salesforce.com/docs/atlas.en-us.216.0.sfdx_dev.meta/sfdx_dev/sfdx_dev_test_data_example.htm



<a name="SFwebsite"></a>

### Configure the API connection between the website and Salesforce

@Dan?


<a name="Changes"></a>

## G) Plan changes, update test scripts

1. Draft a description of what the system will look like when you're done. This can be a picture of an altered form or report.

2. Define commit messages for the sequence of changes. This can provide a roadmap for estimating effort and timelines.

3. Define the tests for each feature added or changed.

4. We believe in the advantages of a "test first" approach. Create test scripts to validate new fields that have not yet been created. If the change is removal of a field, write a "negative" test to verify the absence of the field among a list. Then code changes that cause the test to pass.


<a name="TestDeploy"></a>

## I) Run tests, make changes, and deploy

1. Run a test of the existing test suite to ensure that everything works.

2. Define what changes you would like to make, in small increments of commit

   * If it's a form, take a picture of the form, paste it in PowerPoint or Google GSuite and add the field.
   * Plan out the commits that you'll be making to get to done.
   * Review with others regularly. Here is an opportunity for all sides to learn something new, and be better friends.
   <br /><br />

3. Create a branch, named beginning with your assigned user name followed by a dash and number.

4. Make changes to the test suite, and make commits.

5. Create a Pull (Merge) Request:

   Please send a [GitHub Pull Request to opengovernment](https://github.com/opengovernment/opengovernment/pull/new/master) with a clear list of what you've done (read more about [pull requests](http://help.github.com/pull-requests/)). When you send a pull request, we will love you forever if you include test code. We can always use more test coverage. Please follow our coding conventions (below) and make sure all of your commits are atomic (one feature per commit).

   Always write a clear log message for your commits. One-line messages are fine for small changes, but bigger changes should contain a paragraph describing what changed and its impact:

   <pre>git commit -m "A brief summary of the commit"</pre>

5. Change the test suite and make sure it runs to success.

   Please consider the people who will read your code, and make code reable for them.
   We optimize for readability:

   * Indent Bash shell files using three spaces (soft tabs).
   * Use HAML for all views.
   * Avoid logic in views, putting HTML generators into helpers.
   * Put spaces after list items and method parameters (`[1, 2, 3]`, not `[1,2,3]`), around operators (`x += 1`, not `x+=1`), and around hash arrows.
   <br /><br />

6. Visually review with others while it's in your unit test environment.

7. Check the new branch into GitHub (or whatever version control repository your team uses).

8. Others make comments on the code.

9. One of the leads moves the branch into a test org and run more tests.

   https://github.com/ipoconnection/ipo-web/blob/master/TESTS_README.md

10. One of the leads deploys the change into production, then run <strong>post-deploy</strong> tests.

John Henry put together some short videos demonstrating our use of Salesforce in Classic. It is not down to the specific fields and record types. https://loom.com/share/folder/860745ad51354264973f438589c2228d

## Other CONTRIBUTE.md files on the internet

* https://www.firsttimersonly.com/
* https://kbroman.org/github_tutorial/pages/fork.html
* https://github.com/firstcontributions/first-contributions
* https://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project
* https://akrabat.com/the-beginners-guide-to-contributing-to-a-github-project/
* https://gist.github.com/MarcDiethelm/7303312

