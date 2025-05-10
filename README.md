(May 10th)  
New Repo. Old repo pkamath2-website.    
Why? Old MBP (2019) stopped booting! For no reason. I guess it had enough. It just didnt feel like waking up one fine morning. Temperamental thing that one.    
Bought a new macbook (Apple Silicon).   
Trusty Old Hugo does not work on Apple Silicon (Gah!). Lost template and data (Double Gah!).   
Remade from scratch.   
Worst few days.   
Better now.   
Alls well.   

<br>
<br>
<br>
<br><br>
<br>
      
      
        
     

hugo serve <-- To run the local server  
hugo <-- Build for distribution  
hugo deploy --maxDeletes 0 <-- Push to S3. MaxDeletes is important. Risk of a wipeout if not. (See Double Gah!)  
Checkout https://purnimakamath.com  

## Dear lord, why aren't my changes visible??
1. Did you invalidate cloudfront cache? If not wait 24 hours.    
2. Check your cloudfront origin - is it set to <domain name>-s3-website-<region> like url? Subfolders default paths dont work unless origin is setup like this. This should not change - but oh well you never know..   
3. Check the toml file, are you pushing to the right bucket?   
