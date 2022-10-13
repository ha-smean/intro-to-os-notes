# intro-to-os-notes

## sep 29 | notes

```
null terminator is part of the string, so the "s" asccii value has two bits
```



copy bytes, copying method: 
```
memcpy
```

how to store a list of entries? 
```
//entry *entries = malloc(size0f(entry) * 3000000);
entry *entries[300000]; //puts them in the statck
```

make code faster: 

![image](https://user-images.githubusercontent.com/88512549/193122963-c36fbaa7-f653-47fa-af76-c013831721fd.png)



____________________________________________________________

## reading one byte at a time

```Ruby
#include <fcntl.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>

/*
 * Read from a file and print the contents
 */

int main (int argc, char **argv) {

	const char * filename = "emoji.txt";
	int readval;
	int fd = open(filename, O_RDONLY);

	// check for errors
	
	// Read one byte at a time
	
	unsigned char buf;
	readval = read(fd, &buf, 1);
	printf("The byte: %c\n", buf);
	
	unsigned char emoji[5]; // Null terminator
	readval = read(fd, emoji, 4);
	// null terminator?>?
	emoji[4] = '\0';
	printf("The byte: %s->5\n", emoji);

	close(fd);

	return 0;
}
```

## Makefile


check the manual of makefile
man makefile


## lecture | oct 13

























