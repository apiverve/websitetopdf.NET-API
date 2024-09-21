Website to PDF API
============

Website to PDF is a simple tool for converting a website to PDF. It returns the PDF file generated from the website.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a .NET Wrapper for the [Website to PDF API](https://apiverve.com/marketplace/api/websitetopdf)

---

## Installation

Using the .NET CLI:
```
dotnet add package APIVerve.API.WebsitetoPDF
```

Using the Package Manager:
```
nuget install APIVerve.API.WebsitetoPDF
```

Using the Package Manager Console:
```
Install-Package APIVerve.API.WebsitetoPDF
```

From within Visual Studio:

1. Open the Solution Explorer.
2. Right-click on a project within your solution.
3. Click on Manage NuGet Packages...
4. Click on the Browse tab and search for "APIVerve.API.WebsitetoPDF".
5. Click on the APIVerve.API.WebsitetoPDF package, select the appropriate version in the right-tab and click Install.


---

## Configuration

Before using the websitetopdf API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Website to PDF API documentation is found here: [https://docs.apiverve.com/api/websitetopdf](https://docs.apiverve.com/api/websitetopdf).  
You can find parameters, example responses, and status codes documented here.

### Setup

###### Authentication
Website to PDF API uses API Key-based authentication. When you create an instance of the API client, you can pass your API Key as a parameter.

```
// Create an instance of the API client
var apiClient = new WebsitetoPDFAPIClient("[YOUR_API_KEY]", true);
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var queryOptions = new WebsitetoPDFQueryOptions {
  marginTop = 0.4,
  marginBottom = 0.4,
  marginLeft = 0.4,
  marginRight = 0.4,
  landscape = false,
  url = "https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts"
};
```

###### Simple Request

```
var response = apiClient.Execute(queryOptions);
if(response.error != null) {
	Console.WriteLine(response.error);
} else {
    var jsonResponse = JsonConvert.SerializeObject(response, Newtonsoft.Json.Formatting.Indented);
    Console.WriteLine(jsonResponse);
}
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "marginLeft": "0.4in",
    "marginRight": "0.4in",
    "marginTop": "0.4in",
    "marginBottom": "0.4in",
    "landscape": false,
    "pdfName": "0b69c0df-5c25-4144-9294-336097221f63.pdf",
    "expires": 1725356417742,
    "url": "https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts",
    "downloadURL": "https://storage.googleapis.com/apiverve-helpers.appspot.com/websitetopdf/0b69c0df-5c25-4144-9294-336097221f63.pdf?GoogleAccessId=1089020767582-compute%40developer.gserviceaccount.com&Expires=1725356417&Signature=BCTQNzcQ75OKe2OtBB3lk1ONj%2B4fv07c6uuTCS3OFW2cvJsMe6nsHY%2FC5XNQzHjHEc5O5UuQ86euB52jm%2FX6VF0JUg04LlDmkQcF%2BQTrb9tvYORFv3r9%2BMk4uiZSvt8v7%2FifuMAyJcI0jll4Ot7zpCdRejHltJrVHaxYYqYMHq8ClcBhmpcddWuFSAfY5WENGJ%2FPCv9W%2F1LLYKOJu0YOZtOsHuRRs8Q7DZ1Pnk3EajZbhJKwtgpJ%2F7A1b%2F5guOHDJ2DLKN21BMocPZCCBIBOn%2BlEanbx6JBOT%2FE6IzbHlfsVwIoPIFA1osyJVxjskjsmM%2B7LBogJlUP41OA%2BGd25SA%3D%3D"
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.