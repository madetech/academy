# 2. Applications

## Deciding on a deadline for applications

Depending on how many positions we have available to fill for the particular academy cohort, a decision needs to be made early on of the length of time that applications will remain open. When deciding on the closing date for applications, bear in mind that it would be very difficult/unfair to close early. For example, some people may be delaying submitting their application form based on the original deadline. 

The reason this is emphasised is that we easily had enough applications for our Autumn/Winter 2020 cohort a few weeks before applications closed, over 400+ in the end, and the time (and therefore costs) of running a team to review applications, screening calls etc needs to be considered. If possible, we would have closed applications early, but decided against it in the end and took on the extra costs.

## Application submission

We currently use Typeform for the application submissions. Generally, the questions asked are:

1. About you
   1. What is your first name?
   2. What is your last name?
   3. What is your email address?
   4. What is your eligability to work in the UK?
      - British Citizen
      - EEA National (living in the UK with settled or pre-settled status)
      - EEA National (not living in the UK)
      - I do not currently have the right to work in the UK
      - Indefinite Leave to Remain in UK
      - Student Visa
      - Tier 1 General (Highly Skilled) visa holder
      - Tier 1 Post Study Work Visa holder
      - Tier 4 Student Visa
      - Tier 5 Youth Mobility Scheme visa holder
      - UK Ancestry visa holder
      - UK work permit holder for current employer
      - Working Holiday Maker Visa
   5. Are you fluent in spoken and written English?
2. Your application
   1. Are you available to start the Academy full time in <DATE>?
   2. Which location are you applying for?
      - London
      - Manchester
      - Bristol
      - [...any other locations]
   3. What, if any, technologies particularly interest you?
   4. Describe your favourite thing about building software
   5. What excites you the most about joining the Academy program?
   6. What are some of your favourite interests outside of programming? [@TODO - is this still relevant? Shall we remove?]
   7. Please upload a copy of your CV
   8. How did you hear about the program?
      - Search Engine
      - Facebook
      - Twitter
      - LinkedIn
      - University Careers or CS Dept
      - Already knew Made Tech
      - Made Tech Website
      - Hire STEM Women [@TODO are we removing this?]
      - Codebar
      - Ada College
      - Careers fair
      - Coding Black Females

When the application form is submitted, we use Zapier to automate the population of a row in a matching Airtable database, matching up the questions asked to fields in Airtable. 

In addition to the application form data, Airtable will also hold a "status" and "stage" column. Status being either "applied", "rejected" or "offered" and "stage" being one of:

- Application received
- Application confirmation email sent
- Remote test sent
- Remote test submitted
- Remote test marked
- Remote test passed
- Screening call booked
- Screening call completed
- Introduction day invite sent
- Introduction day RSVP'd
- Introduction day booked
- [@TODO please review stages ^]

## Auto-rejection of candidates

Zapier will handle the auto-rejection of candidates based on responses in the application form:

- You cannot fluently speak English
- You're unable to legally work in the UK
  - Accepted:
    - British Citizen
    - EEA National (living in the UK with settled or pre-settled status)
    - Tier 1 General (Highly Skilled) visa holder
    - Indefinite Leave to Remain in UK
  - Not accepted:
    - I do not currently have the right to work in the UK
    - EEA National (not living in the UK)
    - Student Visa
    - Tier 1 Post Study Work Visa holder
    - Tier 4 Student Visa
    - Tier 5 Youth Mobility Scheme visa holder
    - UK Ancestry visa holder
    - UK work permit holder for current employer
    - Working Holiday Maker Visa
- You cannot make the dates for the academy that you have applied for

If any of these criteria are met, Zapier will trigger an email to be sent via Drip to the candidate outlining the reason. Zapier will also update the status of the applicant to "rejected".

## Auto-progression of application

We use Zapier to automatically send a confirmation email to the candidate if they aren't automatically rejected. This email will:

- Include an introductory video with a number of questions and answers

***

For the below; both the sending out of the coding challenge, and the manual scoring of the application form submitted, we just need to decide if we want to do this in a particular order, as we might be able to save budget on sending out Qualified coding links if we disqualify people based on application form submissions first

***

[Leading on from above, the confirmation email could include...]

- Send out details for the coding challenges for the applicant to complete [@TODO as we are charged in Qualified by number of tests, maybe we should manually tag/trigger the sending of these to ensure no spam submissions cause us to be charged in Qualified...]
- [@TODO should we have applicants view/watch the video before applying? Maybe the video will answer some questions for them and they'll choose not to progress?]

## Scoring of application form

If the candidate has "passed" the coding exercise, and met the pass threshold, then we can manually review the application form they submitted. For each of the following questions on the application form, we want to score 1-3 for each:

- What, if any, technologies particularly interest you?
  1. Apparent little effort in answer, or vague answer
  2. Field not relevant, or too generic an answer
  3. Specific technology interests, relevant to full-stack development
- Describe your favourite thing about building software
  1. Apparent little effort in answer
  2. General response without highlighting a favourite
  3. Demonstrates a clear passion and indicates one or more specifics
- What excites you the most about joining the Academy program?
  1. Apparent little effort in answer
  2. General response without highlighting any specifics
  3. Specific features of the Academy have been highlighted

These scores should be tracked in Airtable as separate columns.