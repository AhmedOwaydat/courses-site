## About Site
This is a courses site you can sign up and start to watch courses.

## How it works
Start with 'index.html' page this is the main page.

## For Back-End developers
This section to the back-end developer to know what he need to change.

#general notes
1/Buttons you need to change its type button or submit as you need in code.

#general notes about navbar
1/In pages "index, categoryCourses, courseDetails and coursePreview" if the use is logged in add class "hidden" to div with class "not-signedIn" and remove class "hidden" from div with class "signedIn". and if the user is not logged in add class "hidden" to div with class "signedIn" and remove class "hidden" from div with class "not-signedIn".
2/If the user is logged in all pages that have div with class "signedIn" in image with class "user-Image" change the image source with user image from data base. and change span with class "user-Name" content with user name from database.
3/when press the div with class "signedIn" which contains user name and image should redirect to user to user home page "home.html" and get user data and put his courses in the page.

#login.html
1/This page to manage users to log in the site.
2/You should put your constrains on input fields(email and password).
3/'OR you can Sign up' button not need to change its type this is a hyper-link convert to 'Register' page.

#register.html
1/This page to manage users to register in the site.
2/You should put your constrains on input fields.
3/'OR you can Log in' button not need to change its type this is a hyper-link convert to 'login' page.

#index.html
1/This is the main page review all categories that site has.
2/Remove all in div with class "row" and for each category except div with class "cats-head" -this you can remove or change content as you like- then for each category add this code:
<div class="col-xl-3 col-lg-3 col-md-4 col-12">
    <div class="card">
        <img class="img-fluid card-img" src="images/main img.jpg" alt="category name">
        <div class="card-img-overlay mx-auto">
            <h3 class="card-title">category name</h3>
            <a href="categoryCourses.html">
                <div class="cat-courses mx-auto">
                    <span><img src="https://png.icons8.com/windows/80/000000/visible.png"></span>
                    View Courses
                </div>
            </a>
        </div>
    </div>
</div>
but you should change the image with class "card-img" source with link to image indicates the category, and change "category name" with the real name for the category.
3/The main image for the header background -div with class "header"- you can change to free or opened source image.
4/when press on view course should redirect to 'categoryCourses.html' page that contains all courses in this category.

#categoryCourses.html
1/This page contains all courses in the category that the user redirected from.
2/The main image for the header background -div with class "header"- you can change to free or opened source image.
3/Category name in the header div should be changed in the span with class "track-name".
4/Remove all in div with class "row" except div with class "courses-head" -this you can remove or change content as you like- then for each course add this code:
<div class="col-xl-3 col-lg-3 col-md-4 col-12">
    <a href="courseDetails.html">
        <div class="card mx-auto">
            <div class="mycard-img">
                <div class="card-overlay">
                    <span class="fa fa-play fa-5x"></span>
                </div>
                <img class="card-img-top" src="images/main img.jpg" alt="course Image">
            </div>
            <div class="card-body">
                <h3 class="course-name card-title">course name</h3>
                <hr>
                <p class="course-instructor card-text">name</p>
                <p class="course-duration card-text">duration</p>
                <p class="Watches_number card-text">
                    <span>number</span>
                    views
                </p>
            </div>
        </div>
    </a>
</div>
5/Change course image with class "card-img-top" source with link to image indicates the course.
6/Change heading element content with class "course-name" with the course name.
7/Change the paragraph with class "course-instructor" content with instructor name.
8/Change the paragraph with class "course-duration" content with course duration.
9/Change the span in the paragraph with class "Watches_number" content with number of views.
11/If the user pressed on the course image it should be redirected to 'courseDetails.html' page.

#courseDetails.html
1/This page contains all course details of the course that the user redirected from.
2/Change the heading element h5 with class "category-name" with course category
3/Change the heading element h1 with class "course-name" with the course name.
4/Change course image with class "course-image" source with link to image indicates the course.
5/Change the span content with class "instructor-name" with the instructor name.
6/Change the span content with class "details" with the course details.
7/Change the span content with class "duration" with the course duration.
8/Change the span content with class "views" with the course views number.
9/remove all in div with class "content" and for each lesson in the course add this code:
<li class="lesson">
    lessonX:
    <ul class="lesson-videos">
        <li>video1</li>
        <li>video2</li>
        <li>video3</li>
    </ul>
</li>
but change lessonX with lesson number and the 'li' elements in div with class "lesson-videos" should has the lesson videos names.
10/click on course image should redirect to "coursePreview.html" page.

#coursePreview.html
1/This page view course videos that the user redirected from.
2/Change span with class "course-Name" content with the course name.
3/remove all from div with class "list" and put this code:
<ul>
    <li class="active" url="vids/1.mp4"><span class="number">01 </span>1<span class="time">04:41</span></li>
    <li url="vids/2.mp4"><span class="number">02 </span>2<span class="time">05:19</span></li>
</ul>
but change the url in 'li' element with the video url, change span with class "number" with the video number and change span with class "time" with the video duration.

#home.html
1/This page view course that user enrolled in.
2/Remove all in div with class "row" except div with class "section-name" for each course add this code:
<div class="course col-xl-3 col-lg-3 col-md-4 col-sm-12 col-12">
    <a href="coursePreview.html">
        <div class="card mx-auto">
            <div class="mycard-img">
                <div class="card-overlay">
                    <span class="fa fa-play fa-5x"></span>
                </div>
                <img class="card-img-top" src="images/main img.jpg" alt="course Image">
            </div>
            <div class="card-body">
                <h5 class="course-name card-title">course name</h5>
            </div>
        </div>
    </a>
</div>
but change image with class "card-img-top" source to the course image and change heading element h5 with class "course-name" content to the course name.
3/click on course redirect to "coursePreview.html" page to preview the videos.

#instructorHome.html     //new page
1/This page is content management to the instructor to view his courses and he can add, edit and remove any of them.
2/when press to user name or image redirect to this page if the user is instructor not normal user.
3/"Add Course" button redirect to "addCourseDetails.html" page. this is used to add new course.
4/"Edit Course" button redirect to "toBeEditedCourse.html" page. this is used to edit course.
5/"Remove Course" button when press on it the backend developer should show alert message that he will remove this course if the instructor pressed ok it will be removed

#addCourseDetails.html
1/This page is to add new course details (course name, instructor name, course image, course details)
2/"Next" button should submit and redirect to "addCourseLessons.html" to continue adding the course lessons.
3/"Cancel" button redirect to "instructorHome.html" page.
4/when press to user name or image redirect to this page if the user is instructor not normal user.

#addCourseLessons.html
1/This page is to add new course lessons and videos.
2/I made with javascript when press "add lesson" button will show inputs takes lesson name, number and videos press done put it in the course content list in right part and put lesson information in variable in js called "lessons" you can go to "addCourseLessons.js" to more information, cancel button remove this lesson.
3/you can more lessons by press the same button.
4/"ADD" button should submit and save course to server and details to database.
5/"cancel" button redirect to "instructorHome.html" page
6/when press to user name or image redirect to this page if the user is instructor not normal user.

#delete.html
1/This page is to delete user, instructor, manager or course
2/change span with class "toBeDeleted" content with the thing user need to delete (user, instructor, manager or course)
3/user enter what he need to delete and his password to confirm the deletion.
4/"Delete" button delete what the user need to delete.
5/the user should authorized to delete some things like instructor can only delete course, the manager can delete any thing and normal user can't access this page.
6/"Cancel" button redirect to "index.html" page.

#toBeEditedCourse.html  //new page
1/This page is to choose edit procedure to course(edit information, Add lesson, Delete lesson, Add video, Delete video)
2/when user choose one of them a form is displayed to do some action as shown:
    a)Edit info: The same as "addCourseDetails.html" but here when redirect to it you should send all course data and change the fields value with it when user done and press "Done" button should submit the changes to the database and redirected to home.
    b)Add lesson: The same as "addCourseDetails.html" but here when redirect to it you should send all course data and change the fields value with it when user done and press "Done" button should submit the changes to the database and redirected to home.
    c)Delete lesson show text box to enter lesson number then delete it.
    d)Add video show form to enter lesson name, video name, video number and the video then add it.
    e)delete video show form to enter lesson name and video name then delete it
3/you should add constrains that the fields not null or what you need to do.


#editUserProfile.html
The same as "register.html" but here when redirect to it you should send all user data and change the fields value with it when user done and press "Done" button should submit the changes to the database and redirected to home.

#mangerHome.html
1/This page is content management to the manager to add, edit and remove courses, users, instructors.
2/when press to user name or image redirect to this page if the user is manager not normal user or instructor.
3/"Add Course" button redirect to "addCourseDetails.html" page. this is used to add new course.
4/"Edit Course" button redirect to "toBeEditedCourse.html" page. this is used to edit course.
5/"Remove Course" button redirect to "delete.html" page. this is used to delete course.
6/"Add Instructor" button redirect to "addManagerOrInstructor.html" page. this is used to add new course.
8/"Remove Instructor" button redirect to "delete.html" page. this is used to delete course.
9/"Add Manager" button redirect to "addManagerOrInstructor.html" page. this is used to add new course.
10/"Remove Manager" button redirect to "delete.html" page. this is used to delete course.

#addManagerOrInstructor.html
The same as "register.html" but here the navbar is added and the user added as instructor or manager you can detect it from the button redirected from before.