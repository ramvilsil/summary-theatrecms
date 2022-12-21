<div align="right">

<a href="https://github.com/ramvilsil/" rel="noreferrer"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Octicons-mark-github.svg/2048px-Octicons-mark-github.svg.png" width="36" height="36" alt="GitHub" /></a> &nbsp;
<a href="https://linkedin.com/in/ramvilsil" rel="noreferrer"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" width="36" height="36" alt="LinkedIn" /></a>

</div>

<div align="center">
<h1> Content Management System Code Summary </h1>

<p>Insights and code snippets from my collaboration on the development of a CMS.</p>

<div>
<a href="https://dotnet.microsoft.com/en-us/" target="_blank" rel="noreferrer" ><img src="https://delaplex.com/wp-content/uploads/2020/02/asp-net-mvc-logo-300x200.png" width="120" height="75" alt=".NET" /></a>
</div>

<a href="https://developer.mozilla.org/en-US/docs/Glossary/HTML5" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/html5-colored.svg" width="36" height="36" alt="HTML5" /></a>
<a href="https://www.w3.org/TR/CSS/#css" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/css3-colored.svg" width="36" height="36" alt="CSS3" /></a>
<a href="https://getbootstrap.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/bootstrap-colored.svg" width="36" height="36" alt="Bootstrap" /></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/javascript-colored.svg" width="36" height="36" alt="JavaScript" /></a>
<a href="https://jquery.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/jquery-colored.svg" width="36" height="36" alt="JQuery" /></a>
<a href="https://docs.microsoft.com/en-us/dotnet/csharp/" target="_blank" rel="noreferrer"><img src="https://seeklogo.com/images/C/c-sharp-c-logo-02F17714BA-seeklogo.com.png" width="35" height="37" alt="C#" /></a>
<a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"><img src="https://hub.meltano.com/assets/logos/extractors/mssql.png" width="36" height="36" alt="MSSQL" /></a>
<a href="https://git-scm.com/" target="_blank" rel="noreferrer"><img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" width="36" height="36" alt="Git" /></a>
</div>


## Introduction
I had the opportunity to contribute to create a full-scale MVC Web Application as part of a development team. The project consisted of a management system for a Portland theater. Our team employed Agile/Scrum, with two-week sprints that included planning, daily standups, sprint retrospectives, and review. I worked on various user stories on both the front and backend.


## Stories

I'll go over some stories I worked on.

- <a href="#ui-styling">UI Styling</a>

- <a href="#asynchronous-database-updates-with-ajax">Asynchronous Database Updates</a>

- <a href="#mapping-the-database-with-entity-framework">Mapping the Database</a>

- <a href="#seeding-data-to-the-database">Seeding Data to the Database</a>

### UI Styling


#### Styling the UI with CSS & BootStrap

As the views had been scaffolded, we were left with an auto generated web page that, although functional, lacked the required user-friendly features. To achieve the desired effects of the user story, I was to restructure the page's HTML and create new locally scoped CSS classes.


.cshtml
```
<div class="blog_author-details-delete--mainContainer">

                <!--Author Image-->
                <img class="blog_author-details-delete--authorImage"
                     src="https://images.pexels.com/photos/792051/pexels-photo-792051.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" />

                <!--Author Text-->
                <div class="blog_author-details-delete--authorTextContainer">

                    <!--Text Top Row-->
                    <div class="blog_author-details-delete--mainContainerTopRow">

                        <!--Author Name-->
                        <strong>@item.Name</strong>

                        <!--Social Icons-->
                        <div>
                            <a href="https://facebook.com">
                                <svg xmlns="http://www.w3.org/2000/svg" width="25" viewBox="0 0 512 512"><path d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.78 90.69 226.38 209.25 245V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.31 482.38 504 379.78 504 256z" /></svg>
                            </a>
                            <a href="https://instagram.com">
                                <svg xmlns="http://www.w3.org/2000/svg" width="25" viewBox="0 0 448 512"><path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" /></svg>
                            </a>
                        </div>

                    </div>

                    <!--Author Bio-->
                    <div>
                        @item.Bio
                    </div>

                    <!--Author Joined/Leave Dates-->
                    <div class="blog_author-details-delete--mainBottomButtonsContainer">

                        <div class="blog_author-details-delete--DatesContainer">

                            <div class="blog_author-details-delete--DatesColumn">
                                <strong>Joined Date</strong>
                                <div>@item.Joined</div>
                            </div>

                            <div class="blog_author-details-delete--DatesColumn">
                                <strong>Left Date</strong>
                                <div>@item.Left</div>
                            </div>

                        </div>

                        <!--Right Side - Edit/Delete Buttons-->
                        <div>

                            <button type="button" class="btn btn-success blog_author-details-delete--buttons">
                                <svg xmlns="http://www.w3.org/2000/svg" onclick="location.href='@Url.Action("Edit", "BlogAuthors", new { id = item.BlogAuthorId })'" fill="white" width="25" viewBox="0 0 512 512"><path d="M471.6 21.7c-21.9-21.9-57.3-21.9-79.2 0L362.3 51.7l97.9 97.9 30.1-30.1c21.9-21.9 21.9-57.3 0-79.2L471.6 21.7zm-299.2 220c-6.1 6.1-10.8 13.6-13.5 21.9l-29.6 88.8c-2.9 8.6-.6 18.1 5.8 24.6s15.9 8.7 24.6 5.8l88.8-29.6c8.2-2.8 15.7-7.4 21.9-13.5L437.7 172.3 339.7 74.3 172.4 241.7zM96 64C43 64 0 107 0 160V416c0 53 43 96 96 96H352c53 0 96-43 96-96V320c0-17.7-14.3-32-32-32s-32 14.3-32 32v96c0 17.7-14.3 32-32 32H96c-17.7 0-32-14.3-32-32V160c0-17.7 14.3-32 32-32h96c17.7 0 32-14.3 32-32s-14.3-32-32-32H96z" /></svg>
                            </button>

                            <button type="button" class="btn btn-danger blog_author-details-delete--buttons">
                                <svg xmlns="http://www.w3.org/2000/svg" onclick="deleteAuthor(@item.BlogAuthorId)" fill="white" width="25" viewBox="0 0 448 512"><path d="M135.2 17.7C140.6 6.8 151.7 0 163.8 0H284.2c12.1 0 23.2 6.8 28.6 17.7L320 32h96c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 96 0 81.7 0 64S14.3 32 32 32h96l7.2-14.3zM32 128H416V448c0 35.3-28.7 64-64 64H96c-35.3 0-64-28.7-64-64V128zm96 64c-8.8 0-16 7.2-16 16V432c0 8.8 7.2 16 16 16s16-7.2 16-16V208c0-8.8-7.2-16-16-16zm96 0c-8.8 0-16 7.2-16 16V432c0 8.8 7.2 16 16 16s16-7.2 16-16V208c0-8.8-7.2-16-16-16zm96 0c-8.8 0-16 7.2-16 16V432c0 8.8 7.2 16 16 16s16-7.2 16-16V208c0-8.8-7.2-16-16-16z" /></svg>
                            </button>

                        </div>

                    </div>

                </div>

            </div>
```

The purpose of this page was to present all of the relevant items in the database. The idea was that once the items were "deleted," they would no longer exist on the page. However, these objects were never meant to be deleted from the database, but rather their DateTime "left date" properties were to be updated using the DateTime.Now method upon confirming their deletion. The implementation of this kind of "deletion" didn't occur until later on so this resulted in an empty "left date" area as you can see below. This may not be a significant issue, but it's something I kept in mind because you normally want to write code that works in way that's mindful of future changes.

![Screenshot_20221216_123745](https://user-images.githubusercontent.com/115331883/208185012-d49b3d13-7ed2-40e3-a24d-7eeef2332a22.png)



#### Programming the UI with jQuery

I implemented a modal that would popup when the delete button was clicked to confirm with the user if they intended to delete the database object. To do so, I simply put the modal together with HTML and CSS.

.css
```
.blog_author-index--deleteModalContainer {
    color: black;
    background-color: white;
    border-radius: 3rem;
    width: 40vw;
    height: max-content;
    padding: 2rem;
    display: none;
    flex-direction: column;
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    z-index: 100;
}

.blog_author-index--deleteModalTopRow {
    display: flex;
    justify-content: space-between
}
```

The modal's display attribute was set to none by default. Using jQuery, the modal was programmed to display upon clicking the delete button and to disappear upon confirming deletion or clicking the close button.

.js
```
//Call upon clicking delete button
function deleteAuthor(authorId) {
    //Define delete modal id
    let deleteModal = '#' + authorId + '-deleteModal'
    //Open delete modal css
    $(deleteModal).show();
    $("body").css("overflow-y", "hidden");
    $(".blog_author-index-authorCardContainer, #createNewButton").css("opacity", "0.5");
}

//Call upon clicking x button in modal
function closeModal(authorId, buttonName) {
    //Define delete modal id
    let deleteModal = '#' + authorId + '-deleteModal'
    //Close delete modal - css
    $(deleteModal).hide();
    $("body").css("overflow-y", "visible");
    $(".blog_author-index-authorCardContainer, #createNewButton").css("opacity", "1");

    //Upon clicking the deleteButton removes author from page and database
    if (buttonName == 'deleteButton') {
        //Fade out animation
        $('.' + authorId).fadeOut(500);
```

### Asynchronous Database Updates with AJAX

The objective here is to "remove" the displayed database objects without requiring a page refresh.

Once users click the delete button, a function is called and the id of the database object is passed. 
This is done so that the database object may be targeted correctly on both front and back ends. 

The button's own id "deleteButton" is also passed since the function's purpose is to close the modal, 
so when other buttons like the "closeButton" would be clicked, the function can differentiate
between them and deliver the correct outcome.

.cshtml
```
onclick="closeModal(@item.BlogAuthorId, 'deleteButton')
```
Clicking the delete button would lead the program to this point where the jQuery .ajax()
function is called to perform an asynchronous HTTP request.
The JSON data is posted to the corresponding class controller's method "AsyncDelete". 

.js
```
$.ajax({
            type: "POST",
            url: "/BlogAuthors/AsyncDelete",
            data: { id: authorId },
        })
```

To allow the objects to display on the page, we must ensure that the "Left" property is nullable,
because it cannot be null if it is not nullable, and the idea here is that only objects with
a null "Left" property can display on the page.

.cs
```
public DateTime? Left { get; set; }
```

The "AsyncDelete" method takes the id of the object and creates an instance of it with the data from the database.
DateTime.Now is used to update the "Left" property. The property changes are then saved to the database.

.cs
```
public ActionResult AsyncDelete(int id)
        {
            BlogAuthor blogAuthor = db.BlogAuthors.Find(id);

            blogAuthor.Left = DateTime.Now;

            db.SaveChanges();
```

### Mapping the Database with Entity Framework

#### Creating an Area Model  

.cs
```
public System.Data.Entity.DbSet<TheatreCMS3.Areas.Blog.Models.BlogAuthor> BlogAuthors { get; set; }
```

.sql
```
CREATE TABLE [dbo].[BlogAuthors] (
    [BlogAuthorId] INT            IDENTITY (1, 1) NOT NULL,
    [Name]         NVARCHAR (MAX) NULL,
    [Bio]          NVARCHAR (MAX) NULL,
    [Joined]       DATETIME       NOT NULL,
    [Left]         DATETIME       NULL,
    CONSTRAINT [PK_dbo.BlogAuthors] PRIMARY KEY CLUSTERED ([BlogAuthorId] ASC)
);
```

#### Creating an Area Admin Model
TPH Structure

### Seeding Data to the Database

.cs
```
protected override void Seed(ApplicationDbContext context)
        {
            HeadAuthor.Seed(context);
        }
```

.cs
```
public static void Seed(ApplicationDbContext context)
        {
            var roleManager = new RoleManager<IdentityRole>(new RoleStore<IdentityRole>(context));
            var roleUserManager = new UserManager<ApplicationUser>(new UserStore<ApplicationUser>(context));

            if (!roleManager.RoleExists("HeadAuthor"))
            {

                var modRole = new IdentityRole();
                modRole.Name = "HeadAuthor";
                roleManager.Create(modRole);

                var headauthor = new HeadAuthor { 
                    
                    UserName = "TheHeadAuthor", Email = "headauthor@theatrecms.dev",
                    ViewsPerMonth = 29, AuthorsHired = 3, AuthorsLetGo = 0 };

                string password = "123";

                var HeadA = roleUserManager.Create(headauthor, password);

                if (HeadA.Succeeded)
                {
                    roleUserManager.AddToRole(headauthor.Id, "HeadAuthor");
                }

            }
```
The data table showing seeded data.

![Screenshot_20221216_124911](https://user-images.githubusercontent.com/115331883/208186532-8d11138a-19b7-4280-b124-69cf5c94a295.png)


## Conclusion

Project management is a crucial aspect of programming professionally.
Working in a team and using project management techniques was a wonderful experience for me. It was nice to be able to perform it rather than simply learn about it.

When working on a project that is in the middle of its life cycle, it is important to first grasp the context. The context might be things like the technology being used and the subject of the project itself. You must also acknowledge that the program is not your personal project and that you must execute things in a particular way, even if you don't love the way it's done.

If I could work on this project again, I think looking back there are things I could have implemented in a better way. I believe I could have done better if I had a better understanding of what the following stories would be. I could have been more thoughtful of them during the stories I was working on to make their implementation easier later on. My final takeaway is that I now understand why they say you'll learn most of your skills on the job because I encountered many things that I didn't know exactly how to do but had a general idea of how to do them.


<div align="center"><a href="https://rxvs.dev" rel="noreferrer">Code Summary by Ramon</a></div>
