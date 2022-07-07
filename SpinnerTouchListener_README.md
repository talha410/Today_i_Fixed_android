# Today_i_Fixed_SpinnerTouchListener issue while opening a search dialog fragment

# Problem :

### After writing touch listener for spinner 
when I press/touch spinner then the search dialog fragment opens 3 4 times instead of opening 1 time.


# How you fix it :
After putting some time an effort I come to the point that in overriding touch event of touch listener we also need to put a check for event type. In this way the issue is fixed. 

# Solution :
The simple check is given below that you need to write it in touch event of the listener in which you want to execute your code block.

if (event.action == MotionEvent.ACTION_UP) {
//you can write you code here for example if you want to open some dialog fragment etc
}
