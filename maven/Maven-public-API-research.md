# Maven Public API Market Research

## ICP

1. **Students** with technical know-how are the main potential users of Maven’s public API. They are mid-career professionals, mainly in the technology industry.
2. **L&D Professionals** performing frequent searches for the benefit of their companies & employees (Students).

## ICP Needs & Pain Points

* **Automated Research:** Users browse through Maven’s UI to find Courses, but also want to automate their research for a suitable Course.
* **Complex Filtering:** Their objective is to come up with a shortlist of Courses for their current education needs. To do this effectively, they often need to filter by specific Instructors or Schools they trust, but they first need a way to discover who those Instructors and Schools are without manually clicking through hundreds of pages.
* **Frictionless Access:** Users want to quickly script against the API or plug it into low-code tools without the friction of registering for API keys or managing authentication tokens for public data.
* **Persistent Search:** If a Course is not found in the moment, they may want to come back and repeat that exact same search for an updated list at a later time.

## Benefits

### Students:

The easier the search is, the more accurate, and the better the chance of finding the right Course at the right time. They may integrate Maven with downstream tools such as IFTTT or use in an LLM for research via Model Context Protocol (MCP).

### L&D Professionals:

The better and more tailored the search, the more likely they are to recommend and approve a Course. They may integrate Maven with downstream tools such as Zapier, n8n or their own internal systems.

### Schools and Instructors:

More engagement, highly qualified prospects, and increased sales. Search volume goes up.

### Maven:

Benefits from increased sales, customer satisfaction, and engagement. The API could also be used by Maven to facilitate complex searches in the UI in the future.

## Use Cases

Based on market research, the following use cases have been discovered, in order of popularity:

1. **Discover available Schools**: List all schools or text search by School Name to identify valid inputs for course filtering.
2. **Discover available Instructors**: List all instructors or text search by Instructor Name to identify valid inputs for course filtering.
3. **Find all Courses that satisfy search criteria**: Complex query combining multiple filters.
- Include all Courses on a specific topic: String search on Course Name.
- Include all courses taught by a specific Instructor by Instructor Name.
- Include all Courses that are offered by a specific School: Search by School ID.
- Include all Coursesrated higher than X: Rating >= number.
- Include all Courses that cost less than Y: Price <= number.
- Include all Courses that have an open Cohort between two dates: Start Date >= date <= End Date.
4. **Get details for a specific Course** including open Cohorts
5. **Get details for a specific Cohort**

**Note Public Access**: All data must be accessible without authentication to ensure ease of use for students and tools.
