# Django Cheatsheet [![My Skills](https://skillicons.dev/icons?i=django&theme=dark)](https://skillicons.dev)

Welcome to the Django Cheatsheet repository! This repository serves as a comprehensive reference guide for Django, a high-level Python web framework. Whether you're a beginner learning Django or an experienced developer seeking a quick reference, this cheatsheet is designed to help you build powerful and scalable web applications with ease.

The cheatsheet covers various aspects of Django, including project setup, models, views, templates, forms, authentication, database queries, URL routing, static files, testing, and deployment. Each section provides concise explanations, code snippets, and best practices to assist you in mastering Django's key concepts.

Feel free to explore this cheatsheet to enhance your Django skills, streamline your development process, and create robust web applications. The cheatsheet is written in Markdown format, making it easy to view, copy, and paste into your own projects.

If you have any suggestions or would like to contribute to this cheatsheet, please feel free to open an issue or submit a pull request. Let's collaborate and make this cheatsheet a valuable resource for the Django community!

Happy Django coding!


# Table of Contents

1. [Introduction to Django](#introduction-to-django)
2. [Django Installation](#django-installation)
3. [Django Project Structure](#django-project-structure)
4. [Creating a Django Project](#creating-a-django-project)
5. [Django Apps](#django-apps)
6. [Models and Databases](#models-and-databases)
7. [Creating Models](#creating-models)
8. [Defining Model Fields](#defining-model-fields)
9. [Migrations](#migrations)
10. [Django Admin](#django-admin)
11. [Registering Models in Admin](#registering-models-in-admin)
12. [URL Patterns and Routing](#url-patterns-and-routing)
13. [Django Views](#django-views)
14. [Function-Based Views](#function-based-views)
15. [Class-Based Views](#class-based-views)
16. [Templates and Template Language](#templates-and-template-language)
17. [Template Variables and Filters](#template-variables-and-filters)
18. [Template Inheritance](#template-inheritance)
19. [Static Files and Media Files](#static-files-and-media-files)
20. [Django Forms](#django-forms)
21. [Form Validation](#form-validation)
22. [Working with Form Data](#working-with-form-data)
23. [Model Forms](#model-forms)
24. [Form Widgets](#form-widgets)
25. [File Uploads](#file-uploads)
26. [Authentication and Authorization](#authentication-and-authorization)
27. [User Authentication with Django's User Model](#user-authentication-with-djangos-user-model)
28. [Custom User Model](#custom-user-model)
29. [Permissions and Authorization](#permissions-and-authorization)
30. [Django Middleware](#django-middleware)
31. [Working with Sessions](#working-with-sessions)
32. [Caching with Django](#caching-with-django)
33. [Django Signals](#django-signals)
34. [Django Template Tags and Filters](#django-template-tags-and-filters)
35. [Custom Template Tags and Filters](#custom-template-tags-and-filters)
36. [Internationalization and Localization](#internationalization-and-localization)
37. [Django Testing](#django-testing)
38. [Unit Testing with Django](#unit-testing-with-django)
39. [Integration Testing with Django](#integration-testing-with-django)
40. [Test Fixtures](#test-fixtures)
41. [Working with QuerySets](#working-with-querysets)
42. [Filtering QuerySets](#filtering-querysets)
43. [QuerySet Methods](#queryset-methods)
44. [Aggregation and Annotation](#aggregation-and-annotation)
45. [Relationships and Foreign Keys](#relationships-and-foreign-keys)
46. [Many-to-Many Relationships](#many-to-many-relationships)
47. [One-to-One Relationships](#one-to-one-relationships)
48. [Django ORM](#django-orm)
49. [Querying the Database](#querying-the-database)
50. [Creating and Updating Objects](#creating-and-updating-objects)
51. [Deleting Objects](#deleting-objects)
52. [Common Datetime Formats in Django](#common-datetime-formats-in-django)  <!-- Place the new section here -->
53. [Django REST Framework Basics](#django-rest-framework-basics)
54. [Serializers in Django REST Framework](#serializers-in-django-rest-framework)
55. [Authentication and Permissions in Django REST Framework](#authentication-and-permissions-in-django-rest-framework)
56. [API Views and ViewSets](#api-views-and-viewsets)
57. [File Uploads in Django REST Framework](#file-uploads-in-django-rest-framework)
58. [Pagination in Django REST Framework](#pagination-in-django-rest-framework)
59. [Versioning in Django REST Framework](#versioning-in-django-rest-framework)
60. [Django Deployment Best Practices](#django-deployment-best-practices)
61. [Troubleshooting Common Django Issues](#troubleshooting-common-django-issues)


### Common Datetime Formats in Django
When working with datetime fields in a Django project, you have the flexibility to customize the display format of dates and times. Django provides various format codes that you can use to represent datetime values according to your preferences. Below is a list of common datetime formats that you can use in your Django project.

Date Formats
%Y - Year with century (e.g., 2023) <br>
%y - Year without century (e.g., 23) <br>
%m - Month as a zero-padded decimal number (01 to 12) <br>
%b - Abbreviated month name (Jan, Feb, etc.) <br>
%B - Full month name (January, February, etc.) <br>
%d - Day of the month as a zero-padded decimal number (01 to 31) <br>

Example: "2023-04-08" <br>
``` python
DATE_FORMAT = "%Y-%m-%d"
```
Time Formats
`%H` - Hour (24-hour clock) as a zero-padded decimal number (00 to 23) <br>
`%I` - Hour (12-hour clock) as a zero-padded decimal number (01 to 12) <br>
`%M` - Minute as a zero-padded decimal number (00 to 59) <br>
`%S` - Second as a zero-padded decimal number (00 to 59) <br>
`%p` - AM or PM  <br>

Example: "15:30:00" <br>

``` python
TIME_FORMAT = "%H:%M:%S"
```

Datetime Formats <br>
`%Y-%m-%d %H:%M:%S` - Datetime with year, month, day, hour, minute, and second (e.g., 2023-04-08 15:30:00) <br>
`%Y-%m-%d %I:%M:%S %p` - Datetime with year, month, day, 12-hour clock, minute, second, and AM/PM (e.g., 2023-04-08 03:30:00 PM) <br>

Example: "2023-04-08 15:30:00" <br>

``` python
DATETIME_FORMAT = "%Y-%m-%d %H:%M:%S"
```
Custom Formats
You can also create custom datetime formats by combining the above format codes and any additional characters you need.

Usage
To apply a datetime format, update the respective format setting in your project's settings.py file. Remember to use these formats within Django's context, such as templates and serializers, to ensure consistent presentation of datetime values.

Feel free to choose the formats that best suit your project's requirements and design.

