GitHub Issue Tracker

Purpose: Auto-tag issues from github automatically or when called

Archtechture: Will use an encorder only transformer model and added choice decoder heads at the end.

Implementation: 
    - Choice will be nn.Linear(h,1) so it will produce only 1 logit.
    - If there are n choices, this will be done n times and options that are above 0.9 threshold will be tagged.
    - RLCD will be used to allign the model to correct choices.
    - Users should have the choice to correct the wrongly chosen tags, active RLCD will be done on the backend to improve the choices.
