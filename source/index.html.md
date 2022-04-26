---
title: Booking API Documentation

language_tabs:
  - java

toc_footers:
  - <a href='https://bookingapi.pricing-coach.com/swagger-ui/index.html' target="_blank">Sign Up for a Developer Key</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Booking API
---

# Booking API Documentation

Welcome to the Pricng-Coach API Documentation! 

Pricing-Coach API is a communication platform that allows sending and receiving information about residences, reservations and prices.

# Reservation Operation

## Add a new reservation


It is the service that should be used to send a new reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
{
  "sellerReservationId": "1",
  "issueDate": "2022-04-03T06:42:19.123Z",
  "reservationDetails": {
      "sellerReservationDetailId": "1",
      "depositPrice": 0,
      "depositPaidAmount": 0,
      "totalPaidAmount": 0,
      "totalPrice": 0,
      "totalRoomPrice": 0,
      "totalFacilityPrice": 0,
      "refundAmount": 0,
      "plannedCheckIn": "2022-04-26T03:16:36.206Z",
      "plannedCheckOut": "2022-04-26T03:16:36.206Z",
      "cancelDate": "2022-04-26T03:16:36.206Z",
      "checkIn": "2022-04-26T03:16:36.206Z",
      "checkOut": "2022-04-26T03:16:36.206Z",
      "reservationStatus": "DEPOSIT",
      "sellerBuildingId": "string",
      "sellerRoomTypeId": "string",
      "reservationSchoolName": "Queen Mary University of London",
      "student": {
        "sellerStudentId": 1,
        "gender": "FEMALE",
        "age": 20,
        "nationality": "UK"
      },
      "invoiceStatus": "UNPAID",
      "invoices": [
        {
          "invoiceId": "12345"
        }
      ],
      "facilities": [
        {
          "sellerReservationFacilityId": "1",
          "name": "Double bed (appr. 135cm*190cm)",
          "price": 39
        }
      ]
    },
  "agent": {
    "name": "A Agent",
    "source": "A Source",
    "responsibleZone": "A Zone"
  }
}
```

> Response:

```json
{
  "message": "string",
  "status": 0,
  "success": true,
  "timestamp": 0,
  "data": {}
}
```

### HTTP Request

`POST https://bookingapi.pricing-coach.com/api/v1/reservations`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
NO_PARAMS 

### Schema (Request)

Name | type | example | description
--------- | ------- | ----------- | -------
sellerReservationId  | string  | 1 |  Id of reservation on seller system
issueDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp at the time of the booking
reservationDetails | ReservationDetail |  | Reservation details for every student
sellerReservationDetailId | string | 1 | Id of reservation detail on seller system.
student | student |  | Reservation Student info
sellerStudentId | string  | 1 | Id of student on seller system
gender | string | FEMALE | Gender of the student
age | 	integer($int32) | 20 | Age of the student"
nationality | string | UK | Nationality of the student
sellerBuildingId | string | 1 | Id of building on seller system.
sellerRoomTypeId | string | 1 | Id of room type on seller system.
reservationSchoolName | string | Queen Mary University of London | School name related with reservation
reservationStatus | string | DEPOSIT | Status of the reservation
invoiceStatus | string | UNPAID | Status of the invoice
invoices | invoice |  | Invoices of the reservation
invoiceId | string | 1 |  Id of invoice on seller system
facilities | facility |  | Facilities related with reservation
sellerReservationFacilityId | string | 1 | Id of the building facility on seller system.
name | string | Double bed (appr. 135cm*190cm) | Name of the building facility 
price | number | example: 39 ; default: 0 | Price of the building facility 
depositPrice | number | 300 | Deposit price of the reservation
depositPaidAmount | number | 255 | Paid amount of the deposit 
totalPaidAmount | number | 500 | Paid amount of the price
totalPrice | number | 500 | Price of the reservation
totalRoomPrice | number | 400 | Total room price of the reservation
totalFacilityPrice | number | 300 | Total facility price of the reservation
refundAmount | number | 300 | Refund amount
plannedCheckIn | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-In timestamp
plannedCheckOut | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-Out timestamp
cancelDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp of the Cancellation 
checkIn | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-In timestamp
checkOut | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-Out timestamp
agent | agent |  | Agent information that received the reservation record
name | string | John Doe | Name of the agent
source | string | Internal | Source of the agent
responsibleZone | string | India | Responsible zone of the agent




### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
message  | string  |   |  Response text
status | string  |   |  Status text
success | boolean   |   | Success status of the response 
timestamp | string($date-time)  | 2022-04-03T06:42:19.123Z  | Timestamp of the  response time
data | string  |   |  


## Update reservation

It is the service that should be used to update a reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
{
  "sellerReservationId": "1",
  "issueDate": "2022-04-03T06:42:19.123Z",
  "reservationDetails": {
      "sellerReservationDetailId": "1",
      "depositPrice": 0,
      "depositPaidAmount": 0,
      "totalPaidAmount": 0,
      "totalPrice": 0,
      "totalRoomPrice": 0,
      "totalFacilityPrice": 0,
      "refundAmount": 0,
      "plannedCheckIn": "2022-04-26T03:16:36.206Z",
      "plannedCheckOut": "2022-04-26T03:16:36.206Z",
      "cancelDate": "2022-04-26T03:16:36.206Z",
      "checkIn": "2022-04-26T03:16:36.206Z",
      "checkOut": "2022-04-26T03:16:36.206Z",
      "reservationStatus": "DEPOSIT",
      "sellerBuildingId": "string",
      "sellerRoomTypeId": "string",
      "reservationSchoolName": "Queen Mary University of London",
      "student": {
        "sellerStudentId": 1,
        "gender": "FEMALE",
        "age": 20,
        "nationality": "UK"
      },
      "invoiceStatus": "UNPAID",
      "invoices": [
        {
          "invoiceId": "12345"
        }
      ],
      "facilities": [
        {
          "sellerReservationFacilityId": "1",
          "name": "Double bed (appr. 135cm*190cm)",
          "price": 39
        }
      ]
    },
  "agent": {
    "name": "A Agent",
    "source": "A Source",
    "responsibleZone": "A Zone"
  }
}
```

> Response:


```json
{
  "message": "string",
  "status": 0,
  "success": true,
  "timestamp": 0,
  "data": {}
}
```

### HTTP Request

`PUT https://bookingapi.pricing-coach.com/api/v1/reservations`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
NO_PARAMS 

### Schema (Request)

Name | type | example | description
--------- | ------- | ----------- | -------
sellerReservationId  | string  | 1 |  Id of reservation on seller system
issueDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp at the time of the booking
reservationDetails | ReservationDetail |  | Reservation details for every student
sellerReservationDetailId | string | 1 | Id of reservation detail on seller system.
student | student |  | Reservation Student info
sellerStudentId | string  | 1 | Id of student on seller system
gender | string | FEMALE | Gender of the student
age | 	integer($int32) | 20 | Age of the student"
nationality | string | UK | Nationality of the student
sellerBuildingId | string | 1 | Id of building on seller system.
sellerRoomTypeId | string | 1 | Id of room type on seller system.
reservationSchoolName | string | Queen Mary University of London | School name related with reservation
reservationStatus | string | DEPOSIT | Status of the reservation
invoiceStatus | string | UNPAID | Status of the invoice
invoices | invoice |  | Invoices of the reservation
invoiceId | string | 1 |  Id of invoice on seller system
facilities | facility |  | Facilities related with reservation
sellerReservationFacilityId | string | 1 | Id of the building facility on seller system.
name | string | Double bed (appr. 135cm*190cm) | Name of the building facility 
price | number | example: 39 ; default: 0 | Price of the building facility 
depositPrice | number | 300 | Deposit price of the reservation
depositPaidAmount | number | 255 | Paid amount of the deposit 
totalPaidAmount | number | 500 | Paid amount of the price
totalPrice | number | 500 | Price of the reservation
totalRoomPrice | number | 400 | Total room price of the reservation
totalFacilityPrice | number | 300 | Total facility price of the reservation
refundAmount | number | 300 | Refund amount
plannedCheckIn | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-In timestamp
plannedCheckOut | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-Out timestamp
cancelDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp of the Cancellation 
checkIn | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-In timestamp
checkOut | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-Out timestamp
agent | agent |  | Agent information that received the reservation record
name | string | John Doe | Name of the agent
source | string | Internal | Source of the agent
responsibleZone | string | India | Responsible zone of the agent




### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
message  | string  |   |  Response text
status | string  |   |  Status text
success | boolean   |   | Success status of the response 
timestamp | string($date-time)  | 2022-04-03T06:42:19.123Z  | Timestamp of the  response time
data | string  |   |  


# Londonist Reservation Information
It is the service that should be used to pull all the reservation records  in the seller system. It is expected to be developed by the seller system. Expected data structure is exemplified. 

It was developed to be run once for the first integration.

##  Get Reservation Information
It is the service that should be used to pull all reservation records for a certain year and month. For this reason, it should be called with year and month values as parameters.



> Request:

```json
{
  "sellerReservationId": "1",
  "issueDate": "2022-04-03T06:42:19.123Z",
  "reservationDetails": {
      "sellerReservationDetailId": "1",
      "depositPrice": 0,
      "depositPaidAmount": 0,
      "totalPaidAmount": 0,
      "totalPrice": 0,
      "totalRoomPrice": 0,
      "totalFacilityPrice": 0,
      "refundAmount": 0,
      "plannedCheckIn": "2022-04-26T03:16:36.206Z",
      "plannedCheckOut": "2022-04-26T03:16:36.206Z",
      "cancelDate": "2022-04-26T03:16:36.206Z",
      "checkIn": "2022-04-26T03:16:36.206Z",
      "checkOut": "2022-04-26T03:16:36.206Z",
      "reservationStatus": "DEPOSIT",
      "sellerBuildingId": "string",
      "sellerRoomTypeId": "string",
      "reservationSchoolName": "Queen Mary University of London",
      "student": {
        "sellerStudentId": 1,
        "gender": "FEMALE",
        "age": 20,
        "nationality": "UK"
      },
      "invoiceStatus": "UNPAID",
      "invoices": [
        {
          "invoiceId": "12345"
        }
      ],
      "facilities": [
        {
          "sellerReservationFacilityId": "1",
          "name": "Double bed (appr. 135cm*190cm)",
          "price": 39
        }
      ]
    },
  "agent": {
    "name": "A Agent",
    "source": "A Source",
    "responsibleZone": "A Zone"
  }
}
```


### HTTP Request

`GET https://bookingapi.pricing-coach.com/api/v1/londonist/reservations/{year}/{month}`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
year | string | true | year information
month | string | true | month information

### Schema (Request)

Name | type | example | description
--------- | ------- | ----------- | -------
sellerReservationId  | string  | 1 |  Id of reservation on seller system
issueDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp at the time of the booking
reservationDetails | ReservationDetail |  | Reservation details for every student
sellerReservationDetailId | string | 1 | Id of reservation detail on seller system.
student | student |  | Reservation Student info
sellerStudentId | string  | 1 | Id of student on seller system
gender | string | FEMALE | Gender of the student
age | 	integer($int32) | 20 | Age of the student"
nationality | string | UK | Nationality of the student
sellerBuildingId | string | 1 | Id of building on seller system.
sellerRoomTypeId | string | 1 | Id of room type on seller system.
reservationSchoolName | string | Queen Mary University of London | School name related with reservation
reservationStatus | string | DEPOSIT | Status of the reservation
invoiceStatus | string | UNPAID | Status of the invoice
invoices | invoice |  | Invoices of the reservation
invoiceId | string | 1 |  Id of invoice on seller system
facilities | facility |  | Facilities related with reservation
sellerReservationFacilityId | string | 1 | Id of the building facility on seller system.
name | string | Double bed (appr. 135cm*190cm) | Name of the building facility 
price | number | example: 39 ; default: 0 | Price of the building facility 
depositPrice | number | 300 | Deposit price of the reservation
depositPaidAmount | number | 255 | Paid amount of the deposit 
totalPaidAmount | number | 500 | Paid amount of the price
totalPrice | number | 500 | Price of the reservation
totalRoomPrice | number | 400 | Total room price of the reservation
totalFacilityPrice | number | 300 | Total facility price of the reservation
refundAmount | number | 300 | Refund amount
plannedCheckIn | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-In timestamp
plannedCheckOut | string($date-time) | 2022-04-03T06:42:19.123Z | Planned Check-Out timestamp
cancelDate | string($date-time) | 2022-04-03T06:42:19.123Z | Timestamp of the Cancellation 
checkIn | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-In timestamp
checkOut | string($date-time) | 2022-04-03T06:42:19.123Z | Actual Check-Out timestamp
agent | agent |  | Agent information that received the reservation record
name | string | John Doe | Name of the agent
source | string | Internal | Source of the agent
responsibleZone | string | India | Responsible zone of the agent

### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
message  | string  |   |  Response text
status | string  |   |  Status text
success | boolean   |   | Success status of the response 
timestamp | string($date-time)  | 2022-04-03T06:42:19.123Z  | Timestamp of the  response time
data | string  |   |  


# Dynamic Pricing Operation
New prices generated by dynamic pricing algorithm are sent to the seller system.

##  Room type price update (Simulate for Londonist)
It is the service that should be used to update the price of spesific residence and room type for the specified dates. There is no need to enter any parameters when calling this service.

It is expected to be developed by the seller system. Expected data structure is exemplified.



> Request:

```json
{
  "roomTypePriceUpdates": [
    {
      "sellerBuildingId": "1",
      "sellerRoomTypeId": "1",
      "price": 225,
      "currency": "£",
      "year": 2022,
      "timeUnit": "WEEK",
      "timeNumber": 20
    }
  ]
}
```

> Response:

```json
{
  "message": "string",
  "status": 0,
  "success": true,
  "timestamp": 0,
  "data": {}
}
```

### HTTP Request

`PUT https://bookingapi.pricing-coach.com/api/v1/londonist/price`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
year | string | true | year information
month | string | true | month information

### Schema (Request)

Name | type | example | description
--------- | ------- | ------- | -----------
roomTypePriceUpdates | RoomTypePriceUpdate |  | Room types whose price will be updated
sellerBuildingId | string | 1 | Id of the building on seller system.
sellerRoomTypeId | string | 1 | Id of the room type at building on seller system.
price | number | 250 | Price info
currency | string | POUND | Price currency info
year | integer($int32) | 2022 | Price Year info
"timeUnit | string | example: WEEK
default: WEEK | Time unit. WEEK or DAY"
timeNumber | integer($int32) | 20 | from 1 to 53 (for week) ;  from 1 to 366 (for day).

### Schema (Response)


Name | type | example | description
--------- | ------- | ----------- | -------
message  | string  |   |  Response text
status | string  |   |  Status text
success | boolean   |   | Success status of the response 
timestamp | string($date-time)  | 2022-04-03T06:42:19.123Z  | Timestamp of the  response time
data | string  |   |  


# Residence Operation
It is used to return information about residences, properties of residences, room types of residences, properties of room types and prices according to weeks.

## Get all residence 
It is the service that should be used to get all information about residences and room types. There is no need to enter any parameters when calling this service.

It is expected to be developed by the seller system. Expected data structure is exemplified.

It was developed to be run once for the first integration.

> Request:

```json

```

> Response:

```json
[
  {
    "sellerBuildingId": "1",
    "name": "Coopers Court",
    "logo": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg",
    "zip": "E3 4SX",
    "address": "10 - 14 Maplin Street, Londra, E3 4SX",
    "longitude": "51.52521976560122",
    "latitude": "-0.032749152989101096",
    "description": "Settle into your studies at Coopers Court in London’s vibrant East End, close to Shoreditch, Victoria Park and the bustling streets of the City",
    "provider": {
      "name": "A Provider"
    },
    "roomTypes": [
      {
        "sellerRoomTypeId": "1",
        "name": "Double En-suite",
        "description": "Mile End tube station is a moment’s walk from your student accommodation. Take the tube or bus to universities and colleges, like London School of Economics or University College London.",
        "roomTypeImages": [
          {
            "imageLink": "https://image.student.com/max_1250x700/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
          }
        ],
        "roomTypeCapacities": [
          {
            "totalRoomCount": 10,
            "totalStudentCount": 20,
            "year": 2022,
            "timeUnit": "WEEK",
            "timeNumber": 20,
            "availableRoomCount": 5,
            "availableStudentCount": 10
          }
        ],
        "roomTypePrices": [
          {
            "price": 225,
            "currency": "£",
            "year": 2022,
            "timeUnit": "WEEK",
            "timeNumber": 20
          }
        ],
        "facilities": [
          {
            "name": "Private bathroom",
            "price": 39,
            "required": true
          }
        ]
      }
    ],
    "buildingImages": [
      {
        "imageLink": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
      }
    ],
    "buildingFacilities": [
      {
        "name": "Entertainment Area/Room",
        "price": 49
      }
    ]
  }
]
```

### HTTP Request

`GET https://bookingapi.pricing-coach.com/api/v1/londonist/residences`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
NO_PARAMS 

### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
sellerResidenceId | string | 1 | Id of building on seller system.
name | string | Coopers Court | Building name
logo | string | https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Building logo
zip | string | E3 4SX | Building zip code
address | string | 10 - 14 Maplin Street, Londra, E3 4SX | Building address
longitude | string | 51.52521976560122 | Building address longitude
latitude | string | -0.032749152989101096 | Building address latitude
description | string | Settle into your studies at Coopers Court in London’s vibrant East End, close to Shoreditch, Victoria Park and the bustling streets of the City | Building description
provider | provider |  | Building owner
name | string | A Provider | name of the provider
roomTypes | RoomType |  | Building room types
sellerRoomTypeId | string | 1 | Id of room type at building on seller system.
name | string | Double En-suite | Room type name
description | string |  Mile End tube station is a moment’s walk from your student accommodation. Take the tube or bus to universities and colleges, like London School of Economics or University College London. | Room type description
roomTypeImages | RoomTypeImage |  | Room type images
imageLink | string | https://image.student.com/max_1250x700/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Room type image link
roomTypeCapacities | RoomTypeCapacitie |  | Room type capacities
totalRoomCount | integer($int32) | 10 | Total room count at specific week
totalStudentCount | integer($int32) | 20 | Total student count that can stay these room at specific week
year | integer($int32) | 2022 | Yer information. From 2020 to 2030
timeUnit | string | example: WEEK ; default: WEEK | Time unit. WEEK or DAY
timeNumber | integer($int32) | 20 | from 1 to 53 (for week) ; from 1 to 366 (for day).
availableRoomCount | integer($int32) | 5 | Available Room Count
availableStudentCount | integer($int32) | 10 | Available Student Count
roomTypePrices | RoomTypePrice |  | Room type prices
price | number | 225 | Price info
currency | string | POUND | Price currency info
year | integer($int32) | 2022 | Price Year info
timeUnit | string | example: WEEK ; default: WEEK | Time unit. WEEK or DAY
timeNumber | integer($int32) | 20 | from 1 to 53 (for week) ; from 1 to 366 (for day).
facilities | facility |  | Room type facilities
name | string | Private bathroom | Facility name
price | number | example: 39 ; default: 0 | Facility price
required | boolean | true | false for optional, true for mandatory facility
buildingImages | BuildingImage |  | Building images
imageLink | string | https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Building image
buildingFacilities | buildingFacility |  | Building facilities
name | string | Entertainment Area/Room | Building facility name
price | number | example: 49 ; default: 0 | Building facility price



## Get residence by id 
It is the service that should be used to get information of spesific residence with residence id, it should be called with residence id value as parameter.

It is expected to be developed by the seller system. Expected data structure is exemplified.

> Request:

```json

```

> Response:

```json
{
  "sellerBuildingId": "1",
  "name": "Coopers Court",
  "logo": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg",
  "zip": "E3 4SX",
  "address": "10 - 14 Maplin Street, Londra, E3 4SX",
  "longitude": "51.52521976560122",
  "latitude": "-0.032749152989101096",
  "description": "Settle into your studies at Coopers Court in London’s vibrant East End, close to Shoreditch, Victoria Park and the bustling streets of the City",
  "provider": {
    "name": "A Provider"
  },
  "roomTypes": [
    {
      "sellerRoomTypeId": "1",
      "name": "Double En-suite",
      "description": "Mile End tube station is a moment’s walk from your student accommodation. Take the tube or bus to universities and colleges, like London School of Economics or University College London.",
      "roomTypeImages": [
        {
          "imageLink": "https://image.student.com/max_1250x700/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
        }
      ],
      "roomTypeCapacities": [
        {
          "totalRoomCount": 10,
          "totalStudentCount": 20,
          "year": 2022,
          "timeUnit": "WEEK",
          "timeNumber": 20,
          "availableRoomCount": 5,
          "availableStudentCount": 10
        }
      ],
      "roomTypePrices": [
        {
          "price": 225,
          "currency": "£",
          "year": 2022,
          "timeUnit": "WEEK",
          "timeNumber": 20
        }
      ],
      "facilities": [
        {
          "name": "Private bathroom",
          "price": 39,
          "required": true
        }
      ]
    }
  ],
  "buildingImages": [
    {
      "imageLink": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
    }
  ],
  "buildingFacilities": [
    {
      "name": "Entertainment Area/Room",
      "price": 49
    }
  ]
}
```

### HTTP Request

`GET https://bookingapi.pricing-coach.com/api/v1/londonist/residences/{id}`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
id | string | true | it's existing residence id


### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
sellerResidenceId | string | 1 | Id of building on seller system.
name | string | Coopers Court | Building name
logo | string | https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Building logo
zip | string | E3 4SX | Building zip code
address | string | 10 - 14 Maplin Street, Londra, E3 4SX | Building address
longitude | string | 51.52521976560122 | Building address longitude
latitude | string | -0.032749152989101096 | Building address latitude
description | string | Settle into your studies at Coopers Court in London’s vibrant East End, close to Shoreditch, Victoria Park and the bustling streets of the City | Building description
provider | provider |  | Building owner
name | string | A Provider | name of the provider
roomTypes | RoomType |  | Building room types
sellerRoomTypeId | string | 1 | Id of room type at building on seller system.
name | string | Double En-suite | Room type name
description | string |  Mile End tube station is a moment’s walk from your student accommodation. Take the tube or bus to universities and colleges, like London School of Economics or University College London. | Room type description
roomTypeImages | RoomTypeImage |  | Room type images
imageLink | string | https://image.student.com/max_1250x700/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Room type image link
roomTypeCapacities | RoomTypeCapacitie |  | Room type capacities
totalRoomCount | integer($int32) | 10 | Total room count at specific week
totalStudentCount | integer($int32) | 20 | Total student count that can stay these room at specific week
year | integer($int32) | 2022 | Yer information. From 2020 to 2030
timeUnit | string | example: WEEK ; default: WEEK | Time unit. WEEK or DAY
timeNumber | integer($int32) | 20 | from 1 to 53 (for week) ; from 1 to 366 (for day).
availableRoomCount | integer($int32) | 5 | Available Room Count
availableStudentCount | integer($int32) | 10 | Available Student Count
roomTypePrices | RoomTypePrice |  | Room type prices
price | number | 225 | Price info
currency | string | POUND | Price currency info
year | integer($int32) | 2022 | Price Year info
timeUnit | string | example: WEEK ; default: WEEK | Time unit. WEEK or DAY
timeNumber | integer($int32) | 20 | from 1 to 53 (for week) ; from 1 to 366 (for day).
facilities | facility |  | Room type facilities
name | string | Private bathroom | Facility name
price | number | example: 39 ; default: 0 | Facility price
required | boolean | true | false for optional, true for mandatory facility
buildingImages | BuildingImage |  | Building images
imageLink | string | https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg | Building image
buildingFacilities | buildingFacility |  | Building facilities
name | string | Entertainment Area/Room | Building facility name
price | number | example: 49 ; default: 0 | Building facility price



