# org.autoplot.SandboxSecurity Manager which allows Autoplot access to:<ul>
 <li>read and write files under HOME/autoplot_data
 <li>read and write files under HOME/.java/.userprefs
 </ul>
 
 Imagined attacks which are still possible:<ul>
 <li> this does nothing to prevent a non-blacklisted file 
 (for example /home/jbf/.profile) and then a post to send the data to
 a remote site.
 </ul>
 
 Presently this just logs access.  Level FINER implies that the property 
 access would be okay, and FINE implied this needs to be studied more.
Sandbox( )


***
<a name="enterSandbox"></a>
# enterSandbox
enterSandbox(  ) &rarr; void

lock down this thread and all child threads so that they cannot do damage
 to the running system.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=enterSandbox&unscoped_q=enterSandbox">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSandboxManager"></a>
# getSandboxManager
getSandboxManager(  ) &rarr; SecurityManager

return a security manager which allows:<ul>
 <li>read from anywhere besides a blacklist
 <li>write to anywhere in whitelist
 <li>any network activity
 <li>any property read
 </ul>
 This is likely to change from the implementation as things develop, so
 please review this code if you must know precisely, or perform 
 experiments until you are satisfied with its operation.

### Returns:
a java.lang.SecurityManager


<a href="https://github.com/autoplot/dev/search?q=getSandboxManager&unscoped_q=getSandboxManager">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

