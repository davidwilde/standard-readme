## Specification

### Requirements

A compliant README must:
  - Be called README.md (with capitalization).
  - Be a valid Markdown file.
  - Sections must appear in order delineated below. Optional sections may be omitted.
  - Must be new lines between each section.

**Suggestions:**
- A "Back to Top" link for longer sections can be useful, but is not required by any means.

### Sections

#### Title
**Status:** Required.  
**Requirements:**
- Must match repository name. If it cannot, there must be a note in the long description about why.
- Must match package manager name. If it cannot, there must be a note in the long description about why.

**Suggestions:**
- Should be self-evident.

#### Banner
**Status:** Optional.  
**Requirements:**
- Must link to local image in current repository.
- Must appear directly after the title.

#### Badges
**Status:** Optional.  
**Requirements:**
- Must be newline delimited.

#### Short Description
**Status:** Required.  
**Requirements:**
- Must be less than 120 characters.
- Must start with `> `
- Must be on it's own line.
- Must match the description in the packager manager's `description` field. 
- Must match GitHub's description (if on GitHub).

**Suggestions:**
- Use [gh-description](https://github.com/RichardLitt/gh-description) to set and get GitHub description.
- Use `npm show . description` to show the description from a local [npm](https://npmjs.com) package.

#### Long Description
**Status:** Optional.  
**Requirements:**
- Must have no heading.

**Suggestions:**
- If too long, consider moving to the [Background](#background) section.
- Cover the main reasons for building the repository.
- "This should describe your module in broad terms,
generally in just a few paragraphs; more detail of the module's
routines or methods, lengthy code examples, or other in-depth
material should be given in subsequent sections.

  Ideally, someone who's slightly familiar with your module should be
able to refresh their memory without hitting "page down". As your
reader continues through the document, they should receive a
progressively greater amount of knowledge."

  ~ [Kirrily "Skud" Robert, perlmodstyle](http://perldoc.perl.org/perlmodstyle.html)


#### Table of Contents
**Status:** Required by default, optional for READMEs less than 100 lines.
**Requirements:**
- Must link to all Markdown sections in the file.
- Must start with the next section; do not include the title or Table of Contents headings.
- Must be at least one-depth: must capture all `##` headings.

**Suggestions:**
- May capture third and fourth depth headings. If it is a long ToC, these are optional.

#### Security
**Status**: Optional.  
**Requirements:**
- May go here if visibility of security section is important. Otherwise, should be in [Extra Sections](#extra-sections).

#### Background
**Status:** Optional.  
**Requirements:**
- Cover motivation.
- Cover abstract dependencies.
- Cover intellecutal provenance: A `See Also` section is also fitting.

#### Install
**Status:** Required by default, optional for doc modules.
**Requirements:**
- Code block illustrating how to install.

Subsections:
- `Dependencies`. Required if necessary.
- `Updating`. Optional.

**Suggestions:**
- Link to prerequisite sites for language: [npmjs](https://npmjs.com), [godocs](https://godoc.org), etc.
- Include any system-specific information needed for Installation.
- Subsection for dependencies needed for install to work.
- If there is no code in the module - for instance, a document-based module - this section is not required.

#### Usage
**Status:** Required by default, optional for doc modules.
**Requirements:**
- Code block illustrating common usage.
- If CLI compatible, code block indicating common usage.
- If importable, code block indicating both import functionality and usage. 

Subsections:
- `CLI`. Required if CLI functionality exists.
- If relevant, point to a runnable file for the usage code.

**Suggestions:**
- Cover basic choices that may affect usage: for instance, if JavaScript, cover promises/callbacks, ES6 here.
- If there is no code in the module - for instance, a document-based module - this section is not required.

#### Extra Sections
**Status**: Optional.  
**Requirements:**
- None.

#### API
**Status:** Optional.  
**Requirements:**
- Describe exported functions and objects.

**Suggestions:**
- Describe signatures, return types, callbacks, and events.
- Cover types covered where not obvious.
- Describe caveats.
- If using an external API generator (like go-doc, js-doc, or so on), point to an external `API.md` file. This can be the only item in the section, if present.

#### Contribute
**Status**: Required.  
**Requirements:**
- State where users can ask questions.
- State whether PRs are accepted.
- List any requirements for contributing; for instance, having a sign-off on commits.

**Suggestions:**
- Link to a contributing or contribute file -- if there is one.
- Be as friendly as possible.
- Link to the GitHub issues.
- Link to Code of Conduct. This is often in Contribute, or organization wide, so may not be necessary for each module.

#### License
**Status:** Required.  
**Requirements:**
- State license initials or name.
- State license owner.
- Must be last section.

**Suggestions:**
- Link to longer License file in local repository.
