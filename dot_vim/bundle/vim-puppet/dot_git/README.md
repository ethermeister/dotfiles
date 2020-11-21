# Git templates

This allows versioned githooks for the whole team. They will need to do the 
following to get it working on their machines.

    git clone https://git.yb.lmax/techops-puppet/git_templates.git ~/.git_templates
    git config --global init.templatedir '~/.git_templates'
    


Afterward, new repositories you create or clone will use this directory for 
templates. Existing repositories can be reinitialized with the proper templates 
by running ``git init`` in the same directory ``.git`` is in.



Create a folder in the repo root called ``.git_hooks`` and put you hooks in 
there and they will be versioned with the rest of your project. 


This works because the template for ``.git/hooks`` contains symlinks that link 
to the respective hooks in ``.git_hooks``.



