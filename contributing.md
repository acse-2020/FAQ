# Contributing to the ACSE FAQ

Please contribute to this FAQ by asking questions and offering answers. Everyone is encouraged to
participate in building a knowledge-base of information regarding the ACSE course and links to
useful external resources.

If this is the first time you have either used git or opened a pull request into a repository,
congratulations - you are learning a critical software carpentry skill! Do not worry about getting
things wrong or making mistakes if you are not experienced in this process. That is one of the 
reasons we use github for this FAQ, to give everyone a chance to work with pull requests in an
environment where support is proactively available and any confusions or mistakes are regarded as
learning opportunities.

## Adding a question

To add a question, create a branch, edit the FAQ to add your question, then open a draft pull
request from your branch into the 'main' branch.

The steps involved in creating a branch and opening a pull request are [documented in detail at docs.github.com]
(https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests).

When creating a new branch, use the form '<username>/<description>' where <username> is your
github username, and <description> is a brief summary of your question. For example, if your 
username is 'zq8653' and your question is regarding extensions in Visual Studio Code you might
call your branch:
  
```
zq8653/VisualStudioCodeExtensions
```

To edit the FAQ, you can either use the web interface at github.com to edit and commit changes
to files, or you can check out the FAQ repository to your local computer, make and commit your
changes, and push them back to github.com. 

You are encouraged to [use the git book as a reference](https://git-scm.com/book/en/v2) if you 
opt for the second method. Whilst it involves more work for you, it is a very important skill
to become proficient at for the ACSE course, and this is an ideal opportunity to learn in a
supported environment.

When you ask your question you may or may not already have an answer to the question. If you do
not have an answer, and want others to help you find an answer, open your pull request as a draft
pull request. If you have both a question and a proposed answer that you are ready for reviewers
to read and comment on, open the pull request as ready for review.

If you want to be actively involved with managing and reviewing your pull request, you are encouraged
to add yourself as a reviewer on the upper right hand side of your pull request page on github.com.

## Answering open questions

Open the [list of open, draft pull requests](https://github.com/acse-2020/FAQ/pulls?q=is%3Apr+is%3Aopen+draft%3Atrue).

Draft pull requests are waiting to be answered, and will be changed to 'ready for review' when an
answer has been contributed.

You can add your voice to the pull request by commenting on the pull request or by adding a commit
to the branch that the pull request has been opened from.

Comments on the pull request are a good way to contribute if you have ideas for how the question might 
be answered but don't feel you are in a position to actually contribute an answer. Perhaps you have
insights into the environment which has led to the question being asked, or have a partial answer
and want input from others to develop it into a full answer.

If you are ready to write an answer to a question, you can do so as a commit to the branch that the
question has been asked and pull requested from. You are strongly encouraged to commit answers to 
questions even if you only know part of an answer - when everyone contributes their knowledge, the
community benefits and gets stronger. It is also a great way to practise your use of git and github
and learn about repository and software management techniques.

If you commit an answer or part of an answer you are encouraged to describe your input in the commit
message but can also use the pull request comments thread if you want to add comments outside of the
commit.

Once a question has a proposed full answer and is ready for review, the pull request can be changed from
draft to 'ready for review'. You can also assign specific reviewers if you want to, or have been asked
to, from the 'reviewers' box on the upper right side of your pull request page on github.com.

## Reviewing answers to a question

Once a question has an answer proposed, it should be marked as 'ready for review', and can be seen
[in this list of open, ready for review pull requests](https://github.com/acse-2020/FAQ/pulls?q=is%3Apr+is%3Aopen+draft%3Afalse).

If you are listed as a reviewer for a question, either because you asked the question, had a similar
question, or were asked to comment on the answer, please look at the changes proposed in the pull
request (see the 'files changed' tab on the pull request page at github.com), read them carefully,
and add comments to the discussion thread for the pull request.

If you have specific changes you'd like to be made, either add them as commits directly to the 
branch that the pull request has been opened from, or describe the changes in your comments.

When reviewers are happy that the answer is complete and correct, they should 'approve' the pull
request to indicate that they are ready for the question and answer to be added to the main branch
of the FAQ.

## Modifying an existing answer

If you want to modify an existing answer, perhaps correcting a mistake or adding more information,
you can do this by opening a new pull request into the main branch of the FAQ repository.

If the branch that the question was originally asked from is still active, you could edit it with
your proposed changes and open a new pull request from it. If the branch no longer exists, you will
need to create a new branch, following the same process described above for adding a new question.

