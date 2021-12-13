# LOG4J2-3201-hot-fix
hot fix replace all jndi 、 rmi 、ldap
kick off jndi expr
lines 132:
```
 value = value.replaceAll("(?i)jndi", "j_n_d_i");
 value = value.replaceAll("(?i)ldap","l_d_a_p");
 value = value.replaceAll("(?i)rmi","r_m_i");
 ```
 lines 152:
 ```
 result = result.replaceAll("(?i)jndi", "j_n_d_i");
 result = result.replaceAll("(?i)ldap","l_d_a_p");
 result = result.replaceAll("(?i)rmi","r_m_i");
 ```
**use (?i) because ${JnDi or ${JNDi etc.. will cause injection the same as ${jndi.**
