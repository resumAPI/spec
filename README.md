# spec
the resumAPI spec

### About
resumAPI is intended to facilitate effortless hiring and job applications. It does this by dropping all the glitz and glamour, and focusing instead on the data. The specification provides a standardized structure, primarily in JSON (although it is format agnostic), that allows individuals to publish their resume/CV data via a web API endpoint. An individual could self-host their their endpoint, or host it on platforms such as GitHub pages, enabling potential employers to retrieve their complete resume/CV using a format that remains consistent across applicants. Access to such endpoints can be restricted through single-use tokens, enabling the user to define the scope and time frame of access. Firms have the opportunity to simplify their job application processes, with the primary application process revolving around providing a valid resumAPI endpoint, ensuring structured, consistent data input that can easily be integrated into their systems. The key advantage is the standardization of data, enabling firms to effortlessly assimilate and process it. Individuals, too, benefit from streamlined job applications, which will reduce the stress of the job application process and enable them to apply to a wider range of opportunities.

### Resume Endpoints

`GET /{username}/resumAPI`

The resume endpoint offers a holistic representation of an individual's professional and academic journey. Comprising fields such as `personal_info`, `education`, `employment`, `teaching`, `publications`, `volunteering`, `certifications`, `skills`, `projects`, `awards`, and `references`, it aims to provide a thorough snapshot of one's experiences and achievements. A salient feature of this specification is its permissiveness; all listed fields are optional, allowing users to customize their data presentation based on their unique profiles and preferences. While the current fields cater to a wide range of professions, the spec acknowledges that careers in specific industries or niches might require further bespoke fields. Fields related to art portfolios, patents, sports achievements, performance metrics, clinical trials, or even legislative contributions might be necessary additions in future iterations. This adaptability is at the heart of resumAPI, ensuring that it remains inclusive and comprehensive for all users across various domains.

Here is an example of a resume endpoint using JSON:

```json
{
    "personal_info": {
        "full_name": "James Dean",
        "contact": {
            "email": "james.dean@email.com",
            "phone": "+1-234-567-8901",
            "address": "123 Hollywood Blvd, Los Angeles, CA"
        },
        "summary": "Experienced actor and cultural icon...",
        "social_links": {
            "linkedin": "https://www.linkedin.com/in/jamesdean",
            "github": "https://github.com/jamesdean"
        }
    },
    "education": [
        {
            "degree": "Bachelor's in Drama",
            "institution": "UCLA",
            "start_date": "1947-09-01",
            "end_date": "1951-06-01",
            "description": "Learned about drama..."
        }
    ],
    "employment": [
        {
            "position": "Actor",
            "company": "Warner Bros",
            "start_date": "1954-01-01",
            "end_date": "1955-09-30",
            "description": "Played a leading role in ..."
        }
    ],
    "teaching": [
        {
            "position": "Drama Teacher",
            "institution": "New York Drama School",
            "start_date": "1952-02-01",
            "end_date": "1953-12-31",
            "description": "Taught drama to undergraduate students..."
        }
    ],
    "publications": [
        {
            "title": "Drama and Life",
            "publisher": "Hollywood Publications",
            "publication_date": "1954-05-01",
            "description": "A look into the life and drama..."
        }
    ],
    "volunteering": [
        {
            "position": "Mentor",
            "organization": "Los Angeles Theatre Club",
            "start_date": "1952-06-01",
            "end_date": "1954-06-01",
            "description": "Mentored young actors and provided guidance..."
        }
    ],
    "certifications": [
        {
            "title": "Certified Drama Specialist",
            "issuer": "Drama Association of America",
            "issue_date": "1952-01-15",
            "expiration_date": "1962-01-15",
            "description": "Certified for excellence in drama and acting techniques."
        }
    ],
    "skills": [
        "Acting", "Public Speaking", "Drama"
    ],
    "projects": [
        {
            "title": "Drama Theatre Renovation",
            "role": "Project Manager",
            "start_date": "1954-02-01",
            "end_date": "1954-12-01",
            "description": "Led a team of 10 to renovate the old drama theatre in Los Angeles...",
            "link": "http://example.com/project"
        }
    ],
    "awards": [
        {
            "title": "Best Actor",
            "issuer": "Hollywood Film Awards",
            "date_received": "1955-05-01",
            "description": "Awarded for outstanding performance in ..."
        }
    ],
    "references": [
        {
            "name": "John Doe",
            "position": "Director, Warner Bros",
            "contact": {
                "email": "john.doe@email.com",
                "phone": "+1-987-654-3210"
            },
            "relationship": "Worked together on ..."
        }
    ]
}

```
