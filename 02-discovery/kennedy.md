# Instructor Scheduling: Research Data

12 user research notes · 10 bug / process failure reports · Education operations, instructor-scheduling focus

> Fictional data based on the problem: instructors are emailed individually and choose courses on a first-come, first-served basis, which causes confusion when two people pick the same course. The "bug reports" describe failures in the manual process.

## User research notes

**UXR-01 · Amara, instructor, 4 cohorts**
"I replied within ten minutes and still lost the course. Someone else had replied to an older email thread first. Nobody told me for two days."

**UXR-02 · Programme coordinator (scheduling owner)**
"Every term I send over 30 separate emails and track the replies in my inbox. When two people claim the same course, I'm the one who has to say no, one by one."

**UXR-03 · Raj, part-time instructor**
"I teach around a full-time job. By the time I see the email at lunch, the good slots are gone. First come, first served really means whoever's free at 9am."

**UXR-04 · Programme director**
"I can't see who's teaching what until the coordinator puts it together. Last term we announced a course to students before the instructor had actually confirmed."

**UXR-05 · Lina, new instructor, first term**
"I didn't know which courses were still open, so I listed my top three. I got three separate replies over a week telling me each one was taken."

**UXR-06 · Tom, instructor, 6 years**
"Honestly, I like the personal email. It feels like being asked, not assigned. I'd hate for it to turn into a cold form."

**UXR-07 · Instructor focus group (aggregate)**
"Six of eight instructors have double-booked themselves with another commitment, because confirmation came days after they replied. All eight want to see what's available in real time."

**UXR-08 · Kemi, instructor in another time zone**
"The emails go out at 9am UK time. That's 4am for me. I'm last in line every single term just because of where I live."

**UXR-09 · Finance and operations lead**
"Contracts and payments depend on the final schedule. When changes happen over email afterwards, I end up paying the wrong person or issuing contracts twice."

**UXR-10 · Programme coordinator (during selection week)**
"In peak week I spend about 10 hours on scheduling emails alone. Last term one reply-all mistake showed everyone's preferences to the whole group."

**UXR-11 · Dan, instructor**
"I swapped a course with a colleague directly, but the change never made it onto the official list. Students got the wrong instructor's name in their welcome email."

**UXR-12 · Student support lead**
"When instructor assignments change late, we get confused students asking who's teaching and whether their session is still on."

## Bug / process failure reports

**BUG-3011 · Sev: Critical**
Courses aren't locked once someone claims them, so two instructors can both believe they've been confirmed for the same course. Each conflict is resolved by hand and takes 3 to 5 email exchanges on average.

**BUG-3018 · Sev: Critical**
There's no single source of truth. The schedule is spread across separate inbox threads, and the final list is put together by hand. The published schedule contained errors in 2 of the last 3 terms.

**BUG-3024 · Sev: High**
Replies are acknowledged 1 to 4 days after they arrive. Instructors hold slots tentatively in the meantime, which leads to double-booking with outside commitments.

**BUG-3027 · Sev: High**
Instructors can't see which courses are already taken, so they keep requesting courses that aren't available, which creates extra back-and-forth.

**BUG-3033 · Sev: High**
The emails always go out at a fixed time, so instructors in later time zones always get last pick.

**BUG-3039 · Sev: Medium**
Swaps and changes made after confirmation don't flow through to student communications, contracts or payroll.

**BUG-3042 · Sev: Medium**
Group emails risk exposing private information. Instructors' preferences and availability were shown to the whole group in one reply-all incident last term.

**BUG-3047 · Sev: Medium**
There's no record of who claimed what and when. Disputes about who came first depend on comparing email timestamps across separate threads.

**BUG-3053 · Sev: Low**
Course details are sent as a PDF attachment, which is often an outdated version.

**BUG-3058 · Sev: Low**
Instructors who miss the email get no automatic reminder, so the coordinator has to chase non-responders by hand.
