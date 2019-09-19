# Leak report

The strip function allocates memory to the variable result. result is then passed on to is_clean and there stored in the variable cleaned. After we compare the input string with cleaned we no longer need the information in cleaned and can free the memory used by it. But, if the string is empty there is no memory to free so we need to make sure we don't call free(). 


