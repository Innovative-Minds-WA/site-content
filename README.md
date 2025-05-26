# Site Content for Innovative Minds

This site powers a lot of the content seen on the [nnovative Minds website](https://www.innovativemindswa.org/). When contributing, don't push directly to the repository (you probably can't anyways); instead create a pull request and someone will check it for errors, then merge it if it's functional.

## Competitions

This is what the program expects from a competition. All fields are required unless marked with a question mark, in which case they are optional. Take a look at existing competition files if you're confused.

```ts
export type Competition = {
  id: number;
  title: string;
  description: string;
  category: "Mathematics" | "Science" | "Engineering" | "Technology" | "Other";
  level: "Elementary" | "Middle School" | "High School" | "All Levels";
  status: "Open" | "Closed" | "Upcoming";
  registrationDeadline?: string;
  competitionDate?: string;
  prize?: string;
  participants?: string;
  website?: string;
  registration_website?: string;
  featured?: boolean;
};
```

## Staff Bios

To put yourself on the website, on the [about page](https://www.innovativemindswa.org/about), create a new file in the `/staff` directory. The file should be named `firstname-lastname.mdx`, with your first name and last name. The file should be in the format below:

```mdx
---
name: "John Doe"
role: "Director of Money"
id: 5
---

John Doe is a pretty cool guy.
```

The ID is used to sort the cards on the website.
