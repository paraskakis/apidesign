# Maven Public API Market Research

## ICP
1. Students with technical know-how are the main potential users of Maven’s public API. They are mid-career professionals, mainly in the technology industry.
2. L&D Professionals performing frequent searches for the benefit of their companies & employees (Students)

## ICP Needs & Pain Points
* Users browse through Maven’s UI to find Courses, but also want to automate their research for a suitable Course.
* Their objective is to come up with a shortlist of Courses for their current education needs, so that they can then do further research and pick a Cohort to possibly sign up for.
* The current workaround is to browse through the Maven UI. The pain point is that they have to click around a lot and can’t perform complex searches. In any case, the result is a single Course Landing Page that the user has to read through.
* If a Course is not found in the moment, they may want to come back and repeat that exact same search for an updated list at a later time.

## Benefits
### Students:
The easier the search is, the more accurate, and the better the chance of finding the right Course at the right time. They may integrate Maven with downstream tools such as IFTTT or use in an LLM for research via Model Context Protocol (MCP)
### L&D Professionals:
The better and more tailored the search, the more likely they are to recommend and approve a Course. They may integrate Maven with downstream tools such as Zapier, n8n or their own internal systems.
### Schools and Instructors:
More engagement, highly qualified prospects, and increased sales. Search volume goes up,
### Maven:
Benefits from increased sales, customer satisfaction, and engagement. The API could also be used by Maven to facilitate complex searches in the UI in the future.

## Use Cases
Based on market research, the following use cases have been discovered, in order of popularity:
1. Find a Course on a specific topic (string search) 
2. Find all Courses that a specific Instructor teaches.
3. Find all Courses that are offered by a specific School
4. Find a Course rated higher than X (Rating >= number)
5. Find a Course that costs less than Y (Price <= number)
6. Find a Course that has an open Cohort between two dates ( Start Date >= date <= End Date)
7. An arbitrary combination of all criteria (complex query)
