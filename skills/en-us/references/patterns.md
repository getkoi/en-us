# Editing patterns

Consult this reference when a passage feels formulaic or when an apparent pattern might be an intentional choice. Edit for the reader, not for an AI-detector score.

## Start with the point

Before:
> Great question! Let's take a closer look at what happens when the token expires. The server rejects requests with an expired token.

After:
> The server rejects requests with an expired token.

Cut staging such as "Here's the thing," "Let's dive in," and "It's important to note." Preserve a real warning or qualification, but state it directly.

## Keep the fact behind the hype

Before:
> This groundbreaking update unlocks seamless collaboration by letting two people edit the same document at once.

After:
> This update lets two people edit the same document at once.

Keep a technical use of a word that also appears in hype, such as "robust regression." Do not replace an unsupported adjective with an invented benchmark.

## Keep meaningful contrasts

Before:
> The dashboard isn't just a list of jobs; it's a powerful way to see which jobs failed.

After:
> The dashboard shows which jobs failed.

A real contrast carries information:
> The endpoint accepts a job ID, not a user ID.

Keep that distinction. Remove a contrast only when it merely stages the point.

## Preserve distinct items

Before:
> The page has filters for date, owner, and status, giving you flexibility, confidence, and control.

After:
> The page has filters for date, owner, and status.

The first three items name actual filters. The second group adds no specific information. A list is not wrong because it has three items.

## Prefer direct verbs

Before:
> The service performs an evaluation of the request and provides a notification to the owner when validation fails.

After:
> The service evaluates the request and notifies the owner when validation fails.

Use "is," "has," and "can" when they fit. Keep more specific verbs when they add meaning: a service that "simulates a database" does not become a database.

## Reduce qualifiers without changing confidence

Before:
> This change might possibly reduce memory use for some large files.

After:
> This change might reduce memory use for some large files.

Keep "might" and "some large files." They express uncertainty and scope. Separate qualifications such as "may fail only under load" are not redundant.

## Keep the source attached to the claim

Before:
> According to the support team, it is important to recognize that most failed uploads occurred after a timeout.

After:
> The support team says most failed uploads occurred after a timeout.

The support team is still the source, and "most" is still the scope. If a passage says only "experts believe," do not invent names or promote the belief to fact. Retain the attribution unless the task includes resolving or removing unsupported claims.

## Remove repetition across paragraphs

Before:
> The cache avoids repeated database queries.
>
> That is the real benefit.
>
> Avoiding those repeated queries is what makes the cache useful.

After:
> The cache avoids repeated database queries.

Keep a closing sentence that adds a consequence or decision. Cut one that only asks the reader to admire the previous sentence.

## Use formatting to help navigation

Before:
> ## Export options
>
> Export options give you options for exporting.
>
> - **CSV:** CSV exports contain rows and columns.
> - **JSON:** JSON exports preserve nested fields.

After:
> ## Export options
>
> - CSV exports contain rows and columns.
> - JSON exports preserve nested fields.

A useful list can stay a list. Remove redundant labels and decoration without losing information or making comparisons harder.

## Match the reader's context

Context: the reader already knows the deployment failed. They asked what to do next.

Before:
> As we discussed, the deployment failed during the migration. Since the migration failed because of a missing index, the next step is to add the index and rerun the migration.

After:
> Add the missing index, then rerun the migration.

For a standalone incident note, keep the failure and its cause. Brevity depends on what this reader already knows.

## Preserve deliberate choices

An isolated dash, passive sentence, long sentence, formal word, or contraction is not an editing defect. Quotation marks may be added by the user's editor. A normal email greeting is not chatbot residue.

Keep quotations, product names, titles, and passages discussing a phrase as a phrase. Keep genuine humor, hesitation, and asides when they fit the author and purpose. Do not add mistakes or invented personal details to manufacture a human voice.

## Sources and adaptations

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing): background for the pattern categories.

The examples are original. EN-US uses contextual editing judgments, allows useful punctuation, protects factual claims and modality, and returns only the finished text by default.
