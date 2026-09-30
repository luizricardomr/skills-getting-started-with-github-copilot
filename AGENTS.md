# Repository Guidance

- This repository is a GitHub Copilot learning exercise. Follow the active material in [.github/steps/](.github/steps/) and its checks in [.github/workflows/](.github/workflows/); avoid changing exercise content unless asked.
- The FastAPI app and in-memory activity state live in [src/app.py](src/app.py). The static UI is plain HTML, JavaScript, and CSS in [src/static/](src/static/); keep API behavior and UI rendering in sync.
- For participant-management changes, update the server-side activity state through an API endpoint and reflect successful changes in the page, including participant lists and remaining capacity. Handle API errors and encode activity names and email values in requests.
- Run the app from the repository root with `python -m uvicorn app:app --reload --app-dir src`.
- Put backend tests in `tests/` and use `pytest`. Add `pytest` to [requirements.txt](requirements.txt) when introducing the test suite, as required by [Step 4](.github/steps/4-step.md). Run `python -m pytest` after changes that affect backend behavior.
- See the [application README](src/README.md) for the API overview; prefer updating or linking existing docs over duplicating them here.