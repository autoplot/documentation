Purpose: notes for transitioning to using Netbeans 7.3.

Audience: Developers using Netbeans

# Introduction

It's time to upgrade to 7.3. There have been known issues with earlier
versions of Netbeans that make upgrading non-trivial. 7.3 still has
issues, but this documents them.

# rebase

  - when this product is first imported into NB 7.3, it will make
    changes to the project files that cause things to break. These
    changes should be reverted in VirboAutoplot/nbproject.
