
# DailyPress – Newspaper Management System

**Roziya Shahin Al-Balushi** – roziyashahin3@outlook.com

**Platform:** OutSystems Reactive Web Application  
**Developed During:** Rihal OutSystems Internship – 2026

## Overview

DailyPress is a web-based Newspaper Management System developed using OutSystems as the final project of my internship at Rihal.

The application allows users to read local and global news, search for articles, and leave comments. It also provides an Admin Panel to manage posts, categories, tags, and comments.

The project was developed to apply OutSystems concepts such as database relationships, CRUD operations, application logic, validation, user roles, API integration, and responsive UI design.

The system includes two main parts:

- **Admin Panel:** Manage posts, categories, tags, and comments.
- **Public Website:** Read local and global news, search articles, and submit comments.

**Application Link:** [Add your DailyPress application URL here]

---

## Database Structure

The application uses a relational database with five main entities:

- **Post:** Stores article information such as title, content, author, category, image, and status.
- **Category:** Stores the different news categories.
- **Tag:** Stores tags used to organize articles.
- **Comment:** Stores user comments on articles.
- **PostTag:** Connects posts and tags through a many-to-many relationship.

### Database Relationships

- One Category can have many Posts.
- One Post can have many Comments.
- One Post can have multiple Tags.
- One Tag can belong to multiple Posts.
- PostTag connects Posts and Tags.

![Database Relationships](screenshots/DatabaseRelationships.png)

---

## Main Features

- Create, read, update, and delete or archive posts.
- Manage news categories and tags.
- Publish articles or save them as drafts.
- Search and filter news articles.
- Pagination and sorting.
- Form validation and required fields.
- Comment submission and moderation.
- Admin access control.
- External API integration for global news.
- Email integration.
- Image upload and handling.
- Responsive UI design using OutSystems and CSS.

---

## Admin Panel

The Admin Panel allows administrators to manage the newspaper system.

It includes the following screens:

- Dashboard
- Posts
- Add Post
- Categories
- Tags
- Comments
- Settings

### 1. Dashboard Screen

![Admin Dashboard](screenshots/AdminDashboard.png)

The dashboard displays a summary of the newspaper system.

- Shows total posts and published posts.
- Displays the number of comments and pending comments.
- Shows recent posts with their categories, tags, and status.
- Allows searching and filtering recent posts.
- Displays categories and their status.
- Provides quick access to create new posts.

#### Comment Moderation and Popular Tags

![Dashboard Comment Moderation](screenshots/DashboardComments.png)

- Displays recent comments that need approval.
- Allows administrators to approve or reject comments.
- Shows popular tags and their related post counts.
- Provides quick access to comment and tag management.

### 2. Posts Management Screen

The Posts screen allows administrators to view and manage news articles.

- View all posts with their title, category, author, status, and tags.
- Search for posts by title or author.
- Filter posts by category, tag, status, and date.
- View, edit, publish, or archive posts.
- Navigate to the Add Post screen.

![Posts Management](screenshots/PostsManagement.png)

### 3. Add Post Screen

![Add Post](screenshots/AddPost.png)

The Add Post screen allows administrators to create new newspaper articles.

The form includes:

- Title
- Short Description
- Article Content
- Category
- Author's Name
- Featured Image
- Tags

#### Validations and Actions

- Required fields must be completed.
- A category must be selected.
- Administrators can upload an article image.
- One or more tags can be assigned to a post.
- Articles can be saved as drafts or published.
- Only published posts appear on the public website.

![Add Post Tags and Summary](screenshots/AddPostDetails.png)

The Post Summary section displays the selected title, category, author, and tags before publishing.

### 4. Category Management Screen

![Category Management](screenshots/Categories.png)

The Categories screen allows administrators to organize newspaper articles into different sections.

- Add new categories with a name and description.
- Edit existing categories.
- Activate or deactivate categories.
- Search categories by name or description.
- Filter categories by status and usage.
- View the number of posts assigned to each category.

### 5. Tag Management Screen

![Tag Management](screenshots/Tags.png)

Tags are used to organize articles by topic.

- Add new tags.
- Edit existing tags.
- Activate or deactivate tags.
- Search and filter tags.
- View the number of posts using each tag.
- Assign multiple tags to one article.

The system uses the PostTag entity to manage the many-to-many relationship between Posts and Tags.

### 6. Comment Management Screen

![Comment Management](screenshots/Comments.png)

The Comments screen allows administrators to review and manage comments submitted by readers.

- View the username, email, comment text, related article, and date.
- Search comments by username, email, or content.
- Filter comments by post, status, and date.
- Approve or reject pending comments.
- Hide or delete comments when needed.

#### Comment Approval Process

![Comment Approval](screenshots/CommentApproval.png)

Comments can have different statuses:

- **Pending:** The comment is waiting for review.
- **Approved:** The comment is accepted and can appear publicly.
- **Rejected:** The comment is not accepted.
- **Hidden:** An approved comment is hidden from public view.

This feature helps administrators control which comments appear on the website.

---

## Public Website

The Public Website allows users to read newspaper articles without accessing the Admin Panel.

It has two main sections:

- Local News
- Global News

### 1. Local News Homepage

![Local News Homepage](screenshots/LocalNews.png)

The Local News section displays articles about Oman.

- Shows featured and breaking news.
- Displays articles from different categories.
- Each article includes an image, title, category, and description.
- Users can open articles to read the full content.
- Users can browse news by category.

#### Latest Local News

![Latest Local News](screenshots/LatestLocalNews.png)

- Displays recent local news articles in cards.
- Shows different topics such as business, education, culture, and technology.
- Allows users to open individual articles.

#### Local News Video Section

![Local News Video](screenshots/LocalNewsVideo.png)

- Displays a featured news video.
- Provides a link to watch the video on YouTube.

### 2. Global News Homepage

![Global News Homepage](screenshots/GlobalNews.png)

The Global News section displays international news using external API integration.

- Retrieves news articles from external sources.
- Displays article images, titles, categories, and descriptions.
- Shows featured international articles.
- Allows users to browse different news categories.

#### Global News Search and Filtering

![Global News Search](screenshots/GlobalNewsSearch.png)

- Search for news articles using keywords.
- Filter articles by category.
- Clear filters to view all articles.
- Open articles to read more details.

#### Latest Global News

![Latest Global News](screenshots/LatestGlobalNews.png)

- Displays recent international articles.
- Shows images, headlines, and news sources.
- Organizes articles into a responsive card layout.

#### Global News Video Section

![Global News Video](screenshots/GlobalNewsVideo.png)

- Displays a featured global news video.
- Allows users to watch the video through YouTube.

### 3. Article Details Screen

![Article Details](screenshots/ArticleDetails.png)

When users select an article, they can view its full details.

- Article title and category.
- Featured image.
- Author and publication information.
- Full article content.
- Related comments.
- Link to the original source for external news articles.

### 4. Comments and Add Comment Form

![Article Comments](screenshots/ArticleComments.png)

Users can read visible comments and submit their own comments.

The Add Comment form includes:

- Name
- Email
- Comment

#### Comment Validation

- Name is required.
- A valid email is required.
- Comment text is required.
- Submitted comments may need administrator approval before appearing publicly.

---

## OutSystems Concepts Applied

### Database and Data Management

- Entities and database relationships.
- One-to-many and many-to-many relationships.
- CRUD operations.
- Aggregates and data queries.
- PostTag relationship handling.

### Application Logic

- Client actions and server actions.
- Variables, lists, and loops.
- Conditional logic.
- Form submission and validation.

### User Interface

- Reactive Web screens.
- Forms and input fields.
- Responsive layouts.
- Custom CSS styling.
- Image and file handling.

### Security and Integrations

- User roles and access control.
- API integration and data handling.
- Email integration.
- Search, filters, and pagination.

---

## Challenges and Learning Experience

During the development of DailyPress, I gained practical experience in building a complete web application using OutSystems.

Some of the main challenges included:

- Creating and managing database relationships.
- Connecting application logic with the user interface.
- Handling multiple tags for each article.
- Implementing validations and comment approval.
- Working with external APIs.
- Fixing errors and improving the website design.

These challenges helped me improve my technical and problem-solving skills.

---

## Conclusion

DailyPress was my final project during my one-and-a-half-month internship at Rihal.

Through this project, I applied many OutSystems concepts in a real web application.

It helped me improve my skills in database design, application development, API integration, and UI design.

The project also gave me valuable experience in testing, solving problems, and improving an application from development to its final result.
