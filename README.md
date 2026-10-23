
**General Notes**

An `onlinecourse` app has already been provided in this repo upon which you will be adding a new assesement feature.

- If you want to develop the final project on Theia hosted by [IBM Developer Skills Network](https://labs.cognitiveclass.ai/), you will need to create the same project structure on Theia workspace and save it everytime you close the browser
- Or you could develop the final project locally by setting up your own Python runtime and IDE
- Hints for the final project are left on source code files
- You may choose any cloud platform for deployment (default is IBM Cloud Foundry)
- Depends on your deployment, you may choose any SQL database Django supported such as SQLite3, PostgreSQL, and MySQL (default is SQLite3)

**ER Diagram**
For your reference, we have prepared the ER diagram design for the new assesement feature.

![Onlinecourse ER Diagram](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database/blob/master/static/media/course_images/onlinecourse_app_er.png)

**Assessment feature**

Learners enrolled in a course can answer its multiple-choice assessment and view a score with feedback for each question. Each submission is tied to the learner's course enrollment. The Django admin lets staff add questions to a course and choices to each question.

To run the project locally on Windows with the Python version specified in `runtime.txt`:

```powershell
py -3.8 -m venv djangoenv
.\djangoenv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver 8001
```

Open `/admin/` to add a course and assessment questions. Learners can enroll from the course list, open the course, and submit its assessment.
