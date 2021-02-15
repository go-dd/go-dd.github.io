---
title: My first Blog Post
description: Learning how to use @nuxt/content to create a blog
img: first-blog-post.jpg
alt: my first blog post

author:
  name: Benjamin
  bio: All about Benjamin
  image: https://images.unsplash.com/.....
---

# My first blog post

Welcome to my first blog post using content module

## This is a heading

This is some more info

### This is a sub heading

This is some more info

### This is another sub heading

This is some more info

## This is another heading

This is some more info

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```


```go


	var jsonMap map[string]interface{}
	if err := json.Unmarshal(body, &jsonMap); err != nil {
		// errorreporting.LogError(err)
		return nil, "", &godd.Error{
			Code:  http.StatusInternalServerError,
			Error: errors.New(response.Status),
		}
	}

    type requestSearchListRead struct {
	Query             string            `json:"query"  swaggertype:"string"         example:"ff"`

func handler() *godd.APIHTTP {
	api := godd.NewAPIHTTP()

	api.ValidateAuth(func(context *godd.Context) *godd.Error {

		svc := (context.Service).(*service)
		token := context.Ctx.Get("X-Access-Token")

		//Validate Auth
		index, err := svc.AuthToken(token)
		if err != nil {
			return err
		}
    }
}

```