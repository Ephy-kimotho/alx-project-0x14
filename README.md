## API overview

The Movies Database API is a RESTful API that provides developers with access to extensive information about movies, TV shows, animations, and more. It offers details such as IMDb ratings, cast and crew information (actors and actresses), release dates, and other relevant data.

## Version

Version 3

## Available Endpoints

- **Favorite Movie** fethces a list of all favorite movies, that a user has liked.
- **Rated TV shows** will fetch all R rated TV shows

## Request and Response Format

All requests are made using the HTTP GET method. For example, to retrieve a list of movies of the upcomimg movies use:
*https://api.themoviedb.org/3/movie/upcoming*
Responses are usualyy in JSON format and and can be used within application easily

## Authentication

To authenticate your requests one needs an API key that is sent in the Authorization headers of the network request made.

## Error Handling

When interacting with the Movies Database API, you may encounter various error responses. Here are some common error scenarios and tips on handling them in your code:

- **400 Bad Request:** This error occurs when the request is malformed or missing required parameters.  
  **Solution:** Double-check the request URL, query parameters, and ensure all required fields are included.

- **401 Unauthorized:** This error indicates that the API key is missing or invalid.  
  **Solution:** Verify that you have included a valid API key in the request header or query parameters.

- **403 Forbidden:** This error means you do not have the necessary permissions to access the resource.  
  **Solution:** Check your API key's permissions and ensure you're accessing endpoints you're authorized for.

- **404 Not Found:** This error occurs when the requested resource (e.g., a movie ID) does not exist.  
  **Solution:** Confirm the resource ID or endpoint URL is correct.

- **500 Internal Server Error:** This indicates an issue on the API's server.  
  **Solution:** Retry the request after a short delay or contact the API support if the problem persists.

## Usage Limits and Best Practices

- **Rate Limits:** The API enforces rate limits to prevent abuse. For example:
  - Free-tier users may be limited to a certain number of requests per minute/hour.
  - Paid plans often include higher request quotas.
- **Data Restrictions:** Some advanced features or datasets may only be accessible on premium tiers.
- **Request Throttling:** Repeated rapid requests may lead to temporary bans or reduced access.
