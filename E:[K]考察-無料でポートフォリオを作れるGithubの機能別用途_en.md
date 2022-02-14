The possible measures are as follows

### Github Pages
It's probably the easiest and easiest way to understand.
It's highly customizable, but since there is no preview, you have to push each article page, wait for the build, and wait until the cache (Github hosting server, not the browser) is updated.
For example, would it be easy to understand if you could have an image of creating a script that picks up raw pages with curl and processes them? It is quite frustrating, so long-term operation is difficult.

### External hosting service cooperation
It has the same problem as Github Pages. It's good to use as a server that is open to the public for production, but like Github Pages, it's not suitable as a development environment.
There are various services such as Netlify and Firebase.

According to Google site speed measurement, it is often faster than Github Pages when accessing from Japan (maybe)

### Gist
Gist's strength is that it can manipulate public settings while not being able to control the order of displayed files.
Public is public as it is, but private is not strictly private and anyone who knows the URL can access it.
If you want to increase the confidentiality, you can manage it in the Github repository and put the information that can be accessed by a specific number of people in Gist.

### Github repository (account name, account name.github.io, etc.)
Unlike the above two, it is updated immediately, and it is great that markdown can be used as it is. (If you specify Github Pages from Theme Chooser, it will be jekyll, you can use markdown, and if you use markdown-wasm etc., it will parse)
However, the layout conforms to the specifications of Github, so there is nothing that can be done in a big way.

### Github Wiki
It's hard to get the impression that you write a profile on a Wiki, but the Wiki system is excellent when viewed as a single site.
For example, [Repository that only summarizes registered profiles] (https://github.com/shimajima-eiji/profile) is easier to read if it is managed in Wiki format rather than source control.

### Github Project
This method is not recommended from the perspective of creating a portfolio. Since the issue is linked to the project, one dedicated repository will be created.
The Beta version shows the page in table / signboard format, so if you can make good use of it, you can do something interesting.

---

### Methods other than Github
Let's compare the means that should be considered, although it deviates from the main point.

#### WordPress (rental server, VPS, etc.)
Commonly used method. It's hard to remember before you get used to it, but it seems to be the most stable in the medium to long term.
Relatively costly (not free)

#### blog
Commonly used method. If it's free, unintended advertisements will be inserted, so it's a shame for a portfolio.
You can pay for it, but I'm not very happy as an engineer because it is dragged by the specifications of each company's service.

#### SNS account (mainly Twitter)
Commonly used method. It's good to know who you are, but it's too troublesome to see (not evaluated)
I'm not good at organizing information, so I should think of some measures.

#### Portfolio service
Recently, there are various portfolio services, but it is difficult to see all of them because they have cut through their own routes.
The famous place is [Linkedin] (https://jp.linkedin.com/).
