Preparing Pull Requests
#######################

1. Fork the
   `climpred_CESM1_S2S GitHub repository <https://github.com/judithberner/climpred_CESM1_S2S>`__.

2. Clone your fork locally using `git <https://git-scm.com/>`_, connect your repository
   to the upstream (main project), and create a branch::

    $ git clone git@github.com:YOUR_GITHUB_USERNAME/climpred_CESM1_S2S.git
    $ cd climpred_CESM1_S2S
    $ git remote add upstream git@github.com:judithberner/climpred_CESM1_S2S.git

    # now, to fix a bug or add feature create your own branch off "main":

    $ git checkout -b your-bugfix-feature-branch-name main

   If you need some help with Git, follow this quick start
   guide: https://git.wiki.kernel.org/index.php/QuickStart

2. Install dependencies into a new conda environment::

    $ conda env update -f climpred_CESM1_S2S.yml
    $ conda activate s2s

3. Break your edits up into reasonably sized commits::

    $ git commit -m "<commit message>"
    $ git push origin your-bugfix-feature-branch-name

4. Find your PR in https://github.com/judithberner/climpred_CESM1_S2S/pulls. See
   changes in notebooks https://app.reviewnb.com/judithberner/climpred_CESM1_S2S/pulls/

5. Now changes in the code can be discussed with comments.

6. Maintainers will merge.
