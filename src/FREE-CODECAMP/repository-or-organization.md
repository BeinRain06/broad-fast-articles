## Github : Repository or Organisation

### Introduction

The first times i was introduced to a github's organization comes from a secondary's school classmate becomes a Tech. I gladly made my first portfolio then he invited me into a newer organization he created for both of us, under the wave of marketing my skills and maybe doing further projects together.
It was so quick, no preliminar good explanations, that even looking at the github documentation i couldn't make sense of the need for a merely portfolio ? I felt unease, but i didn't want to express it. Being tied like a goat on a rope, just left to trust the fact that friendship brought me into it. Since, everytimes i call back this moment , i picture my esteem was left out right from the day of birth of that organization. Then i didn't participate too much on whatever the growing spirit of that one. That made me finally mind to write an article talking about **Repository** and **Organization** in github. A refresher of what users can really ecpect being in an organization or a repository, and also the differences between the both concepts.

### Body

Before continuing you need to have some basic knowledges about `Github` and `Git` version control.

### Overview

We can view **repository** and **organization** as **two separate levels** operation to projects.
One on top level `organization` and the other on bottom `repository`.

![../assets/free-cd-camp-images/picture-1-repo-org.jpg](../assets/free-cd-camp-images/picture-1-repo-org.jpg)

<br/>

### I- Repository

A **Repository** is the basic unit in github . Everyone who opens a _github's account_, also open it first **repository**. Because any github account create a primar and customizable repository who bear your **username**.
A **Repository** is often misunderstood to be a **project** , but it's likely more ~ a **place** where you can store bunch of things : code, images, files , folders in a easier structured way. It is a piece of memory allocated online who hold your root work's case folder for a specific project. Imagine it just as a **box** containing all the files , photos, testimonies , physical evidences that represents the proper investigations of the police under one affair of crime or illegal act affecting citizens under a state .To consider the role of the repository in Tech is to watch the countless applications built everyday. This wouldn't be possible if the entire structure of an app couldn't be trackable and updated. Allowing others people to participate on some of the projects initiated by others. The range of **actions** you can adopt out of a basic stored box for making a living good technology are multiple. We will recap some of these before diving in organization :

Remember, each time you think about **repository** always thinks about **collaboration** and gradually you will grasp the concepts **evolving** around.

You can easily create a repository, in just a few minutes, if you get little knowledge using github. But we aren't talking about repositories's **creation** , we lean rather to provide insights to some basic **actions** you can perform upon these one to better share your work as contributor on solo or collaborative project.

Here are some of the actions you might perform over your **repository** :

### 1.clone

Imagine you made so much change to files inside a project on your computer , and end up messing around , your app return a white blank page, and looking and finding issue for the error print to the terminal, you can seem to catch a solution. Maybe you didn't have a proper internet connection or where implementating new concepts at the spot. This, lead you to a nowhere place.

A downward situation you didn't expect, that would kills your times if all changes has to be undone. You got lazy from your brain and don't want to do that, don't want to navigate in that antartic without a compass : what will be the mission !? On that moment think of **cloning** an **earlier** version of your repository laying in your github account.

This link will explain you more in details how you can **clone** a repository :

[https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

### 2.branch

The fact that you mess up with your code can clearly be avoid if creating a **branch** as soon as possible. Implementing a lot of syntax or code that may not work are more secure if made in a new branch. New concepts, new features update goes the same. Creating a new repository involve creating a **main** branch.

syntax: `git branch -M main`

Any new **branch** that comes after will intend to store the work you are not feeling sure when implementing until you make a move to dissolve it merging it in the **main** branch or deleting it at all. The code syntax manipulation and update will not affect the principal house that is the main branch, the intention is to let your project run but in an set apart chamber. You must create actually more than one branch to test subsequent code . Is all up to you to decide how to manage those, and sent their code in the main branch when they are ready. Any **branch** need to have a proper name describing why it meant to do.

Ensure you **switch** from an ex branch to a new one before continuing writing code on a specific purpose, else the change we remain to the old branch and gives you difficulty to track properly your work or in trouble affect a branchyou did not want to. **git** has command to how **_switch from one branch to another_**, typed in the shell command of your editor.

### 3.pull request

The defense that brings **new branch** from trouble is quite comforting. Now that your change and update are working fine, you need to push these from the current branch you are in to the main branch.
In order to start this process you have to initiate a **pull request**.
This follows a green line that propose your change to the repository main branch. If you are an owner of this repository you will be redirected to **compare and merge** your change. If not, the owner of the repository will go over your change and accept the modification or reach you further by pull request message asking you to make additionnal improvements to some of the narrowed aspects before send it back.
This hierarchy makes the work more collaborative and efficient within many github account working in a repository.

Documentation Pull Request: [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)

### 4.merge

**compare and merge** is the last process you apply to a specific branch if you want your work to be sent over another specific branch especially the main branch. **Comparison** let you look at differences and conflicts between the code you want to merge and the current code laying at each specific file online under the repository. Once conflicts (or if there is no conflict) are resolved, you are good to go , you can merge whatsoever set of update you have made to the repository.

During this process you will also experience how powerful **Git** track changes on a repository.

Github Merge branch : [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)

### 5.Fork

**Fork** is also an act of **copy** as **_clone_**, the difference is that the copy is made online generally from a repository that is not yours to your **repository**. Maybe you have seen some cool features animations one guy made in a github repository and you want it to serves as inspirations over times during your future work. You then fork the repository! Making a copy of this one inside your own onboard online repositories , ready to check anytime you need a guidance. You can update these repositories according to the mainstream update of the owners too. But you can't modify something inside , except you reach the owner with an update in a pull request, wishing it would be applied.

<br/>

### II- Organization

Once we grasp Repository, it is time to look it on **Organization**.

It quite sounds like an `enterprize`. Sure, it is !. While a repository is a place to store code (and you need to have a github account to do that). An **Organization** is a **group of Github Account** representing a team and they work and contribute to repository, open source online, or projects of their own. Their publication are covered under the **organization's** namw not an individual account. This team have a strucure of a company , the work done by team are proposed by managers that set the vision of the team.
Any **decisions** have to be back with the approval of managers who set **permissions** and **right** to each nested team or personal account.
Any members (github's account) has opportunities to start discussion, express their values propositions for a project but are restricted to their access set of rules, granted by owners. Organization enhance several level of security than a regular repository, thatis why they are vital for huge project you need to work on.
Instead of creating a repository in your account , allowing others to shares their update. Many accounts can be grouped into an organization and then in any initiated repository created inside the organization by owners. This process works well to implement product or service in demands fast. Let's bring on what kind of management you could possess creating an **organization** that offers a shelter to many github's account simultaneously.

Before continuing. Just happens to always things of an github **organization** as a **structurate enterprize**

We have two kinds of worker in an enterprize:

- standard employees
- managers

All decisions made in a nested team( or individual account) has to pass the approval of your direct manager(s) to no be consequential on you is something turn down. The manager is supposed to be a guide in the aspect decision making giving you specific advise on where to go , begin , or move on under certain particular problems, or take your proposition as welcoming. As say earlier they might have the vision ,the experience, even if they do not have the right skill to solve the actual problem, but most often they are also skilled to some area of IT skills and their knowledge comes out also as an asset.

Managers in a Github organization are called **organization owner**. And here they possess rights that goes from inviting someone in joining the organization, to managing **access** of all **resources and permissions** that might be granted to individual account or a nested group inside the organization.

For Employees (simple invited account) you are given role according to your skills and this role come also with a set of **permissions** to be not overwhelmed and more often enhance security access on differents aspects of a project. As we usually see in corporation the lower you are on the ladder, the more you don't have access to most decisional directives of the firm.

To recap , being a **part** of an **organization** brings strength level of security in the projects built. You have a wide range of experienced people and that is an asset to scale your growth rapidly, gain trust from others company, participate to side projects that doesn't go in flow with their daily routine of some enterprize needing outsiders for a specific amount of times, and leverage cash for the entire team over the process.

These are freedom or will power while being an **organization owner** :

1. **manage access to the organization**

   > Invite people
   > Give them role
   > Give them level of access

2. **manage access to resources by any nested teams in your organization**

   > Repositories
   > Projects
   > Apps

3. **Configure the organization to meet yor vision and need**
   > Restricts Types of repositories that could be created.
   > Allow members to have cascaded permissions individually and in the nested teams they are involved
   > Bring a scalable level of security to your app, project, and give you the track to focus effort to improve solutions for the matter you are working on or the product you are developing.

![../assets/free-cd-camp-images/picture-2-repo-org.jpg](../assets/free-cd-camp-images/picture-2-repo-org.jpg)

You can have complementary informations about **organization** if you want.

On the github documentation below you view in details why and how and organization can be a good way to scale up, collaborate and build teams.

**About Organization** : [https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations)

If you have more questions or even a feedbacks to this article . Feel free to leave amessage . On

twitter : [https://twitter.com/nest_Ngoueni](https://twitter.com/nest_Ngoueni)

linkedin : [https://www.linkedin.com/in/gerard-ngouend-5a0584244/](https://www.linkedin.com/in/gerard-ngouend-5a0584244/)

Thanks you for your Time.
