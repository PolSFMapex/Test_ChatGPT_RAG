# Test_ChatGPT_RAG

This document is a test to know how much can chatGPT retrive. This is a dummy table:

| ID  | First Name | Last Name  | Email                        | Age | City          | Country         | Occupation          | Joined Date | Last Login  | Status   |
|-----|------------|------------|------------------------------|-----|---------------|-----------------|---------------------|-------------|-------------|----------|
| 1   | Alice      | Smith      | alice.smith@example.com      | 28  | New York      | USA             | Software Engineer   | 2023-01-15  | 2025-06-03  | Active   |
| 2   | Bob        | Johnson    | bob.johnson@example.net      | 34  | London        | UK              | Data Analyst        | 2022-07-22  | 2025-06-01  | Active   |
| 3   | Charlie    | Brown      | charlie.brown@example.org    | 22  | Paris         | France          | Graphic Designer    | 2024-03-10  | 2025-05-28  | Inactive |
| 4   | Diana      | Williams   | diana.williams@example.com   | 45  | Berlin        | Germany         | Project Manager     | 2021-11-05  | 2025-06-04  | Active   |
| 5   | Edward     | Jones      | edward.jones@example.biz     | 30  | Tokyo         | Japan           | Marketing Specialist| 2023-09-01  | 2025-05-15  | Active   |
| 6   | Fiona      | Garcia     | fiona.garcia@example.co.uk   | 29  | Madrid        | Spain           | Teacher             | 2022-02-18  | 2025-06-02  | Active   |
| 7   | George     | Miller     | george.miller@example.info   | 52  | Rome          | Italy           | Architect           | 2020-05-12  | 2024-12-20  | Pending  |
| 8   | Hannah     | Davis      | hannah.davis@example.com     | 38  | Toronto       | Canada          | Nurse               | 2023-06-30  | 2025-06-03  | Active   |
| 9   | Ian        | Rodriguez  | ian.rodriguez@example.net    | 25  | Sydney        | Australia       | Sales Representative| 2024-01-05  | 2025-05-22  | Active   |
| 10  | Julia      | Wilson     | julia.wilson@example.org     | 41  | Amsterdam     | Netherlands     | HR Manager          | 2021-08-19  | 2025-06-01  | Inactive |
| 11  | Kevin      | Martinez   | kevin.martinez@example.com   | 33  | Los Angeles   | USA             | Developer           | 2022-10-10  | 2025-06-04  | Active   |
| 12  | Laura      | Anderson   | laura.anderson@example.biz   | 27  | Chicago       | USA             | Content Creator     | 2023-04-01  | 2025-05-30  | Active   |
| 13  | Michael    | Thomas     | michael.thomas@example.co.uk | 49  | Manchester    | UK              | Consultant          | 2020-12-01  | 2025-03-11  | Pending  |
| 14  | Nora       | Jackson    | nora.jackson@example.info    | 36  | Brussels      | Belgium         | Researcher          | 2022-05-25  | 2025-06-02  | Active   |
| 15  | Oscar      | White      | oscar.white@example.com      | 24  | Vienna        | Austria         | Student             | 2024-02-20  | 2025-05-18  | Active   |
| 16  | Penny      | Harris     | penny.harris@example.net     | 31  | Zurich        | Switzerland     | Financial Advisor   | 2023-03-12  | 2025-06-03  | Active   |
| 17  | Quentin    | Martin     | quentin.martin@example.org   | 40  | Lisbon        | Portugal        | Entrepreneur        | 2021-06-08  | 2025-04-25  | Inactive |
| 18  | Rachel     | Thompson   | rachel.thompson@example.com  | 26  | Dublin        | Ireland         | UX Designer         | 2023-11-15  | 2025-06-01  | Active   |
| 19  | Samuel     | Garcia     | samuel.garcia@example.biz    | 39  | Barcelona     | Spain           | Chef                | 2022-01-30  | 2025-05-29  | Active   |
| 20  | Tina       | Robinson   | tina.robinson@example.co.uk  | 32  | Copenhagen    | Denmark         | Photographer        | 2023-08-08  | 2025-06-04  | Pending  |
| 21  | Umar       | Clark      | umar.clark@example.info      | 47  | Oslo          | Norway          | Engineer (Civil)    | 2020-09-14  | 2025-02-10  | Active   |
| 22  | Violet     | Lewis      | violet.lewis@example.com     | 23  | Helsinki      | Finland         | Intern              | 2024-04-05  | 2025-05-25  | Active   |
| 23  | Walter     | Lee        | walter.lee@example.net       | 55  | Stockholm     | Sweden          | Professor           | 2019-07-21  | 2025-06-02  | Inactive |
| 24  | Xena       | Walker     | xena.walker@example.org      | 37  | Warsaw        | Poland          | Project Coordinator | 2022-09-03  | 2025-05-12  | Active   |
| 25  | Yusuf      | Hall       | yusuf.hall@example.com       | 29  | Prague        | Czech Republic  | IT Support          | 2023-12-22  | 2025-06-03  | Active   |
| 26  | Zoe        | Allen      | zoe.allen@example.biz        | 43  | Budapest      | Hungary         | Operations Manager  | 2021-04-16  | 2025-04-01  | Pending  |
| 27  | Aaron      | Young      | aaron.young@example.co.uk    | 35  | Athens        | Greece          | Scientist           | 2022-06-11  | 2025-05-20  | Active   |
| 28  | Bella      | King       | bella.king@example.info      | 27  | Bucharest     | Romania         | Analyst             | 2023-07-07  | 2025-06-04  | Active   |
| 29  | Caleb      | Wright     | caleb.wright@example.com     | 48  | Sofia         | Bulgaria        | Manager             | 2020-11-27  | 2025-01-15  | Inactive |
| 30  | Daisy      | Scott      | daisy.scott@example.net      | 21  | Zagreb        | Croatia         | Barista             | 2024-05-01  | 2025-05-31  | Active   |
| 31  | Ethan      | Green      | ethan.green@example.org      | 39  | Belgrade      | Serbia          | Electrician         | 2021-10-03  | 2025-06-01  | Active   |
| 32  | Grace      | Adams      | grace.adams@example.com      | 31  | Bratislava    | Slovakia        | Account Executive   | 2023-02-28  | 2025-06-02  | Active   |
| 33  | Henry      | Baker      | henry.baker@example.biz      | 42  | Ljubljana     | Slovenia        | Plumber             | 2022-03-09  | 2025-05-10  | Pending  |
| 34  | Isla       | Nelson     | isla.nelson@example.co.uk    | 26  | Reykjavik     | Iceland         | Tour Guide          | 2023-10-18  | 2025-05-28  | Active   |
| 35  | Jack       | Carter     | jack.carter@example.info     | 50  | Tallinn       | Estonia         | CEO                 | 2019-03-05  | 2025-06-03  | Active   |
| 36  | Lily       | Mitchell   | lily.mitchell@example.com    | 29  | Riga          | Latvia          | Pharmacist          | 2022-08-24  | 2025-06-01  | Inactive |
| 37  | Mason      | Perez      | mason.perez@example.net      | 36  | Vilnius       | Lithuania       | Mechanic            | 2021-02-14  | 2025-05-05  | Active   |
| 38  | Mia        | Roberts    | mia.roberts@example.org      | 24  | Nicosia       | Cyprus          | Waitress            | 2024-01-20  | 2025-05-27  | Active   |
| 39  | Noah       | Turner     | noah.turner@example.com      | 44  | Valletta      | Malta           | Pilot               | 2020-07-07  | 2025-06-04  | Active   |
| 40  | Olivia     | Phillips   | olivia.phillips@example.biz  | 33  | Luxembourg    | Luxembourg      | Banker              | 2022-12-12  | 2025-03-22  | Pending  |
| 41  | Owen       | Campbell   | owen.campbell@example.co.uk  | 28  | Monaco        | Monaco          | Real Estate Agent   | 2023-05-05  | 2025-06-02  | Active   |
| 42  | Sophia     | Parker     | sophia.parker@example.info   | 37  | Andorra la V. | Andorra         | Retail Manager      | 2021-09-09  | 2025-05-19  | Active   |
| 43  | Lucas      | Evans      | lucas.evans@example.com      | 30  | San Marino    | San Marino      | Historian           | 2022-04-14  | 2025-06-01  | Inactive |
| 44  | Ava        | Edwards    | ava.edwards@example.net      | 46  | Vaduz         | Liechtenstein   | Librarian           | 2020-01-10  | 2025-02-28  | Active   |
| 45  | Liam       | Collins    | liam.collins@example.org     | 25  | Bern          | Switzerland     | Social Media Mgr    | 2023-09-27  | 2025-05-30  | Active   |
| 46  | Isabella   | Stewart    | isabella.stewart@example.com | 39  | Ottawa        | Canada          | Government Official | 2021-03-23  | 2025-06-03  | Pending  |
| 47  | Logan      | Morris     | logan.morris@example.biz     | 32  | Canberra      | Australia       | Systems Admin       | 2022-11-08  | 2025-04-17  | Active   |
| 48  | Amelia     | Murphy     | amelia.murphy@example.co.uk  | 27  | Wellington    | New Zealand     | Veterinarian        | 2023-06-16  | 2025-06-04  | Active   |
| 49  | Elijah     | Cook       | elijah.cook@example.info     | 41  | Dublin        | Ireland         | Business Owner      | 2020-10-20  | 2025-01-05  | Inactive |
| 50  | Harper     | Rogers     | harper.rogers@example.com    | 29  | Auckland      | New Zealand     | Flight Attendant    | 2023-01-31  | 2025-05-26  | Active   |
