# ScheduleProject
# ERD
![테이블](<img width="347" alt="스크린샷 2025-03-26 오전 10 10 55" src="https://github.com/user-attachments/assets/0bddaf9f-2a20-4b97-9da8-f5cdd1212a3f" />
)

# API 명세서

|          | Method | URL             | 설명                    | Request                                                                                                             | Response                                                                                                                          | 상태코드      |
|----------|--------|-----------------|-------------------------|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|---------------|
| 일정등록 | POST   | /schedules      | 새 일정을 생성합니다.   | {<br>  "title": "회의",<br>  "start_time": "2025-03-26T10:00:00",<br>  "end_time": "2025-03-26T11:00:00"<br>}       | {<br>  "id": 1,<br>  "title": "회의",<br>  "start_time": "2025-03-26T10:00:00",<br>  "end_time": "2025-03-26T11:00:00"<br>}       | 200: 정상등록 |
| 일정조회 | GET    | /schedules/{id} | 특정 일정을 조회합니다. |                                                                                                                     | {<br>  "id": 1,<br>  "title": "회의",<br>  "start_time": "2025-03-26T10:00:00",<br>  "end_time": "2025-03-26T11:00:00"<br>}       | 200: 정상조회 |
| 일정수정 | PUT    | /schedules/{id} | 기존 일정을 수정합니다. | {<br>  "title": "회의(변경)",<br>  "start_time": "2025-03-26T10:30:00",<br>  "end_time": "2025-03-26T11:30:00"<br>} | {<br>  "id": 1,<br>  "title": "회의(변경)",<br>  "start_time": "2025-03-26T10:30:00",<br>  "end_time": "2025-03-26T11:30:00"<br>} | 200: 정상수정 |
| 일정삭제 | DELETE | /schedules/{id} | 특정 일정을 삭제합니다. |                                                                                                                     | {<br>  "message": "일정이 삭제되었습니다."<br>}                                                                                   | 200: 정상삭제 |
