# Examples and voice

Consult this reference for worked rewrites or voice matching. The examples are fictional and self-contained. Each rewrite uses only the facts in its source or the stated context.

## 1. A verbose chat answer

Before:
> Great question! It's important to note that the export feature gives you the ability to download your invoices in CSV format. In order to get started, navigate to Billing, choose Export, and select the month you need. I hope this helps!

After:
> To download your invoices as CSV:
>
> 1. Open Billing.
> 2. Select Export.
> 3. Choose the month.

Check: the output retains the file format, all three actions, and their order. It omits the conversational wrapper.

## 2. A technical condition

Before:
> If a request times out, the client may retry it up to three times, provided that the request includes an idempotency key; requests without a key must not be retried automatically.

After:
> If a request times out and has an idempotency key, the client may retry it up to three times. Requests without a key must not be retried automatically.

Check: timeout and key requirements both survive. "May," "up to three times," and the prohibition on automatic retries remain. The passive second sentence avoids inventing an actor for that prohibition.

## 3. Uncertain failure

Before:
> The upload may have failed. An interrupted connection could be the cause. It is important to check the log before retrying.

After:
> The upload may have failed. An interrupted connection could be the cause. Check the log before retrying.

Check: the rewrite does not assert a failure or a confirmed cause. It retains the log check before the retry.

## 4. US localization

Before:
> The organisation will analyse colour settings on 28 September 2026. The test costs £1,500.50 and requires a 10 kg weight.

After:
> The organization will analyze color settings on September 28, 2026. The test costs £1,500.50 and requires a 10 kg weight.

Check: spelling and date presentation change. The date, price, currency, and measurement do not. The rewrite need not be shorter when the source is already concise.

## 5. Prose inside a Markdown file

Before:

````markdown
---
title: Colour settings
---

Use `colour_mode` to customise the colour. In order to set it to blue, run:

```sh
app configure --colour=blue
```

See [colour settings](https://example.com/colour-settings).
````

After:

````markdown
---
title: Colour settings
---

Use `colour_mode` to customize the color. To set it to blue, run:

```sh
app configure --colour=blue
```

See [color settings](https://example.com/colour-settings).
````

Check: code, the identifier, frontmatter, and the link destination are unchanged. Visible prose and the link label use US spelling.

## 6. An author's voice

Voice sample:
> I like small tools. If I have to read a manual, I lose interest.

Text to revise:
> I tried the new timer on Monday, and I like that it has just one button. It took me two attempts to pause it, though.

After:
> I tried the new timer on Monday. I like its single button, though it took me two tries to pause it.

Check: the rewrite keeps Monday, the single button, the two attempts, and the mixed reaction. It borrows the sample's direct style without inventing a manual or loss of interest.

When matching a sample, observe sentence length, contractions, vocabulary, punctuation, and transitions. Keep the requested genre. An author's playful blog voice need not turn a technical procedure into a personal essay.

## 7. Already concise

Before:
> Save the file before you close the editor.

After:
> Save the file before you close the editor.

Check: no change is needed. Return the sentence without an explanation of why it stayed the same.

## 8. A clarification that takes more words

Audience: readers who do not know the term "idempotent."

Before:
> Repeating the same request is idempotent.

After:
> Repeating the same request has no additional effect. This behavior is called idempotency.

Check: the result explains the unfamiliar term without inventing how the system implements it. The extra words serve the audience.

## 9. Ambiguous input

Input:
> Localize this date to US English: The release is on 04/05/2026.

Response:
> Does 04/05/2026 mean April 5 or May 4?

Check: a necessary question takes priority over producing a polished but possibly incorrect date.

## 10. Complete coverage

Request:
> Rewrite this list and keep all six formats: The supported export formats that are currently available are CSV, JSON, XML, YAML, TSV, and Parquet.

Response:
> Available export formats: CSV, JSON, XML, YAML, TSV, and Parquet.

Check: all six formats remain. A preference for short lists does not justify removing requested content.

## 11. A list of requirements

Before:
> To access the dashboard, you need an active account, a verified email address, and membership in the workspace.

After:
> Dashboard access requires all three:
>
> - An active account.
> - A verified email address.
> - Workspace membership.

Check: bullets make the requirements easy to scan. The list preserves every requirement and makes clear that each one is necessary.

## Review method

Check a rewrite against its source for meaning, not just word count. Verify each number, condition, qualification, attribution, and ordered action. Compare code and other protected content literally.

Then read for natural rhythm and remove anything that adds no useful information. Prefer the shorter version when both communicate equally well. Keep additional words when they prevent a misunderstanding.
