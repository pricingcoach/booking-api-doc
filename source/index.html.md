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

Welcome to the Booking API! You can use our API to access Booking API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Reservation Operation

## Add a new reservation

Add new reservation endpoint.

> Request:

```json
{
  "sellerReservationId": "1",
  "issueDate": "2022-04-03T06:42:19.123Z",
  "reservationDetail": {
    "sellerReservationDetailId": "1",
    "student": {
      "sellerStudentId": 1,
      "gender": "FEMALE",
      "age": 20,
      "nationality": "UK"
    },
    "sellerResidenceId": "string",
    "sellerRoomTypeId": "string",
    "school": {
      "name": "Queen Mary University of London"
    },
    "reservationSchoolName": "Queen Mary University of London",
    "reservationStatus": "DEPOSIT",
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
    ],
    "depositPrice": 0,
    "depositPaidAmount": 0,
    "totalPaidAmount": 0,
    "totalPrice": 0,
    "totalRoomPrice": 0,
    "totalFacilityPrice": 0,
    "refundAmount": 0,
    "plannedCheckIn": "2022-04-23T19:57:54.220Z",
    "plannedCheckOut": "2022-04-23T19:57:54.220Z",
    "cancelDate": "2022-04-23T19:57:54.220Z",
    "checkIn": "2022-04-23T19:57:54.220Z",
    "checkOut": "2022-04-23T19:57:54.220Z"
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

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------
sellerReservationId | string | 1 | Id of reservation on seller system
issueDate | date | 2022-04-03T06:42:19.123Z | 
reservationDetail | ReservationDetail |   | Reservation details for every student


## Update reservation

Update an existing reservation. It is called instantly when a new reservation is made or changes are made to the existing reservation.

> Request:

```json
{
  "sellerReservationId": "1",
  "issueDate": "2022-04-03T06:42:19.123Z",
  "reservationDetail": {
    "sellerReservationDetailId": "1",
    "student": {
      "sellerStudentId": 1,
      "gender": "FEMALE",
      "age": 20,
      "nationality": "UK"
    },
    "sellerResidenceId": "string",
    "sellerRoomTypeId": "string",
    "school": {
      "name": "Queen Mary University of London"
    },
    "reservationSchoolName": "Queen Mary University of London",
    "reservationStatus": "DEPOSIT",
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
    ],
    "depositPrice": 0,
    "depositPaidAmount": 0,
    "totalPaidAmount": 0,
    "totalPrice": 0,
    "totalRoomPrice": 0,
    "totalFacilityPrice": 0,
    "refundAmount": 0,
    "plannedCheckIn": "2022-04-23T20:09:37.559Z",
    "plannedCheckOut": "2022-04-23T20:09:37.559Z",
    "cancelDate": "2022-04-23T20:09:37.559Z",
    "checkIn": "2022-04-23T20:09:37.559Z",
    "checkOut": "2022-04-23T20:09:37.559Z"
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

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------
sellerReservationId | string | 1 | Id of reservation on seller system
issueDate | date | 2022-04-03T06:42:19.123Z | 
reservationDetail | ReservationDetail |   | Reservation details for every student

# Londonist Reservation Information
Returns reservations made on the londonist system

##  Get Reservation Information
Return matched reservations

> Request:
```json

```

> Response:

```json
[
  {
    "sellerReservationId": "1",
    "issueDate": "2022-04-03T06:42:19.123Z",
    "reservationDetail": {
      "sellerReservationDetailId": "1",
      "student": {
        "sellerStudentId": 1,
        "gender": "FEMALE",
        "age": 20,
        "nationality": "UK"
      },
      "sellerResidenceId": "string",
      "sellerRoomTypeId": "string",
      "school": {
        "name": "Queen Mary University of London"
      },
      "reservationSchoolName": "Queen Mary University of London",
      "reservationStatus": "DEPOSIT",
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
      ],
      "depositPrice": 0,
      "depositPaidAmount": 0,
      "totalPaidAmount": 0,
      "totalPrice": 0,
      "totalRoomPrice": 0,
      "totalFacilityPrice": 0,
      "refundAmount": 0,
      "plannedCheckIn": "2022-04-23T20:17:55.498Z",
      "plannedCheckOut": "2022-04-23T20:17:55.498Z",
      "cancelDate": "2022-04-23T20:17:55.498Z",
      "checkIn": "2022-04-23T20:17:55.498Z",
      "checkOut": "2022-04-23T20:17:55.498Z"
    },
    "agent": {
      "name": "A Agent",
      "source": "A Source",
      "responsibleZone": "A Zone"
    }
  }
]
```

### HTTP Request

`GET https://bookingapi.pricing-coach.com/api/v1/londonist/reservations/{year}/{month}`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
year | string | true | year information
month | string | true | month information

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------


# Dynamic Pricing Operation
New prices generated by dynamic pricing algorithm are sent to the system

##  Room type price update (Simulate for Londonist)
It updates the price for the specified dates for the selected residence and room type.

> Request:

```json
{
  "roomTypePriceUpdates": [
    {
      "sellerResidenceId": "1",
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

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------


# Residence Operation
It returns information about residences, properties of residences, room types of residences, properties of room types and prices according to weeks.

## Get all residence 
Get all residence (Simulate for Londonist)

> Request:

```json

```

> Response:

```json
[
  {
    "sellerResidenceId": "1",
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
    "residenceImages": [
      {
        "imageLink": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
      }
    ],
    "residenceFacilities": [
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

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------


## Get residence by id 
Get residence with residence id (Simulate for Londonist)

> Request:

```json

```

> Response:

```json
{
  "sellerResidenceId": "1",
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
  "residenceImages": [
    {
      "imageLink": "https://image.student.com/450x338/property-78127-3ccc734b0abbbb09eae586b6d5194621.jpeg"
    }
  ],
  "residenceFacilities": [
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

### Schema

Name | type | example | description
--------- | ------- | ----------- | -------
