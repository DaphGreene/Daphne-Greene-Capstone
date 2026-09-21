# Daphne + The Glitches Band App

A Java/Spring Boot coursework capstone built around Daphne + The Glitches.

The application explores a DATG-branded web experience with user registration, authentication, persistent profiles, tour-date management, and band-related content.

Although this project predates my later ideas for a broader DATG companion app / Arcade ecosystem, some of its account and community-facing concepts became relevant to that later thinking. This repository should be understood as a student capstone and early web-application experiment, not as a finished version of that future product concept.

## Built With

- Java 17
- Spring Boot
- Spring Security
- Spring Data JPA
- Thymeleaf
- MariaDB
- HTML / CSS / JavaScript
- Maven

## Current Status

Legacy coursework project, preserved and maintained as a portfolio piece.

The current canonical version has been locally verified to:

- build successfully with Java 17
- start against MariaDB
- register users
- authenticate users
- preserve profile-description changes across logout/login
- create and persist tour-date data
- return users to a previously requested protected page after login
- serve the music route successfully

The repository's Spring context-load test also passes.

The direct-login fallback currently remains a small behavior under review and is separate from the verified saved-request login flow.

## Local Setup

### Requirements

- Java 17
- MariaDB
- Maven wrapper included with the project

### Database

Create a MariaDB database named:

`DATGUsers`

Set the following environment variables before running the application:

`MYSQL_USER`

`MYSQL_PASSWORD`

The repository does not require database credentials to be committed to source control.

### Build

`./mvnw package`

### Run

`./mvnw spring-boot:run`

## Application Features

### Navigation

The application includes:

- Home
- Music
- Tour
- Contact
- Login
- Registration
- Profile access for authenticated users
- Logout

Navigation changes depending on authentication state.

### Home

Landing page with basic band information and visual content.

### Music

DATG music content embedded within the application.

### Tour

Displays tour-date information including:

- city
- venue
- date
- advance ticket price
- day-of-show ticket price

Authenticated users can create, edit, and delete tour-date records.

### Contact

Band contact form collecting:

- name
- email
- message

### Profile

Authenticated users can access a persistent profile and update account-related information.

### Login

Existing users can authenticate with their username and password.

If authentication was triggered by an attempt to access a protected page, Spring Security can return the user to that requested page after login.

### Registration

New users can create an account using:

- email
- username
- password

Successful registration redirects the user to the login page.

## Portfolio Context

This repository is the canonical portfolio-facing version of the capstone.

Other historical copies of the project may preserve earlier development history or coursework snapshots, but this repository represents the version intended for ongoing documentation and portfolio presentation.

## Future Context

Some ideas explored here, particularly user accounts, profiles, and a DATG-centered authenticated experience, overlap conceptually with later thinking around a possible DATG companion app / DATG Arcade ecosystem.

That later product idea remains unresolved, and this capstone should not be treated as its final architecture or implementation.