# Parkrun-API-Python
Python API for Parkrun data

## Python Requirements
```python
pip install requests
pip install beautifulsoup4
```
## Example Usage
```python
import requests
from bs4 import BeautifulSoup
import math

def ExampleUsage():

    # General Setup Data
    countries = Country.GetAllCountries()
    events = Event.GetAllEvents()
    Event.UpdateEventUrls(events, countries)

    selectedEvent = events[0]

    # Event Specific Data
    eventHistory = EventHistory.GetEventHistorys(selectedEvent)
    firstFinishers = FirstFinisher.GetFirstFinishers(selectedEvent)
    ageCategoryRecords = AgeCategoryRecord.GetAgeCategoryRecords(selectedEvent)
    clubs = Club.GetClubs(selectedEvent)
    sub20Women = Sub20Woman.GetSub20Women(selectedEvent)
    sub17Men = Sub17Man.GetSub17Men(selectedEvent)
    ageGradedLeagueRanks = AgeGradedLeagueRank.GetAgeGradedLeagueRanks(selectedEvent)
    fastest500 = Fastest.GetFastest500(selectedEvent)

    # Country Specific Data
    weekFirstFinishers = WeekFirstFinisher.GetWeekFirstFinishersForCountry(countries[0])
    weekSub17Runs = WeekSub17Run.GetWeekSub17RunsForCountry(countries[0])
    weekTopAgeGrades = WeekTopAgeGrade.GetWeekTopAgeGradesForCountry(countries[0])
    weekNewCategoryRecords = WeekNewCategoryRecord.GetWeekNewCategoryRecordsForCountry(countries[0])
    courseRecords = CourseRecord.GetCourseRecordsForCountry(countries[0])
    attendanceRecords = AttendanceRecord.GetAttendanceRecordsForCountry(countries[0])
    mostEvents = MostEvent.GetMostEventsForCountry(countries[0])
    largestClubs = LargestClub.GetLargestClubsForCountry(countries[0])
    joined100Clubs = Joined100Club.GetJoined100ClubsForCountry(countries[0])
    mostFirstFinishes = MostFirstFinish.GetMostFirstFinishesForCountry(countries[0])
    freedomRuns = FreedomRun.GetFreedomRunsForCountry(countries[0])
    historicNumbers = HistoricNumber.GetHistoricNumbersForCountry()

    # Global Results Data
    globalWeekFirstFinishers = WeekFirstFinisher.GetWeekFirstFinishersGlobally()
    globalNewCategoryRecords = WeekNewCategoryRecord.GetWeekNewCategoryRecordsGlobally()
    globalSub17Runs = WeekSub17Run.GetWeekSub17RunsGlobally()
    globalTopAgeGrades = WeekTopAgeGrade.GetWeekTopAgeGradesGlobally()
    globalCourseRecords = CourseRecord.GetCourseRecordsGlobally()
    globalFreedomRuns = FreedomRun.GetFreedomRunsGlobally()

    # Global Stats Data
    globalLargestClubs = Club.GetLargestClubsGlobally()
    globalAttendanceRecords = AttendanceRecord.GetAttendanceRecordsGlobally()
    globalMostEvents = MostEvent.GetMostEventsGlobally()
    globalMostFirstFinishes = MostFirstFinish.GetMostFirstFinishesGlobally()

    print("Done")

ExampleUsage()
```
