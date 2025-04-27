# cse330-project-4-accessing-usb-storage-using-the-block-abstraction-solved
**TO GET THIS SOLUTION VISIT:** [CSE330 Project 4-Accessing USB Storage using the Block Abstraction Solved](https://www.ankitcodinghub.com/product/cse330-operating-systems-project-4-accessing-usb-storage-using-the-block-abstraction-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120977&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE330  Project 4-Accessing USB Storage using the Block Abstraction Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
<h1>Brief Summary</h1>
The block abstraction is a unified translation layer designed by your OS to access different storage devices at the granularity of <em><sub>blocks </sub></em>(e.g., 512 bytes). This abstracts away differences between operations supported by storage devices. For instance, hard disk drives (HDDs) write equal-sized sectors, while solid state drives (SSDs) write at the granularity of a single page or collection of pages, depending on the state of the flash. Please refer to lecture #17 for more details.

Under typical circumstances, the block abstraction is invisible to user programs, which read or write to <em>files</em>. However, it is useful for user programs to have fine-grained control over blocks in some cases. For instance, the <em><sub>dd </sub></em>command in Linux OSs uses the block layer to perform tasks like formatting disks and burning new images. Similarly, the <em><sub>mkfs </sub></em>command initializes a new file system on a storage device using the block abstraction. Both commands are user programs you can execute from the terminal.

In this project, your task is to write a kernel module that allows a user program (i.e., our testcases) to directly access a virtual USB storage device using the block abstraction. Your kernel module should support both read and write operations of different block sizes, and at different offsets.

<ul>
<li>sudo apt update</li>
<li>sudo apt install git</li>
<li>git clone -b TBA https://github.com/ASTERISC-Teaching/cse330-public.git</li>
</ul>
Directory breakdown. The repository contains the following directories: • outputs: Output for all testcases.

<ul>
<li><sub>testcases: </sub>All the testcases for this project.</li>
<li><sub>kmodule: </sub>The skeleton code for the kernel module.</li>
<li><sub>sh: </sub>Script that allows you to run a test.</li>
</ul>
<table width="623">
<tbody>
<tr>
<td width="116">Important note</td>
<td width="507"></td>
</tr>
<tr>
<td colspan="2" width="623">•&nbsp;&nbsp; This document only contains high-level instructions for completing this project; they are NOT EXACT step-by-step instructions. You MUST figure out the steps on your own.

•&nbsp;&nbsp; This project requires you to use the kernel (Linux v6.6.9) you compiled in project #1. If you
</td>
</tr>
</tbody>
</table>
are changing your group, it is okay to get the VM disk from your previous group and use it.

<ul>
<li>Remember to add debug statements inside the kernel module (e.g., using printk) to see what your code is doing and debug the operations. This applies to all steps of the project.</li>
<li>We provide you all testcases but it is your job to understand what these testcases are doing.</li>
<li>If your assignment does not compile or your upload is corrupted, you will get a zero.</li>
</ul>
Always double-check your submission.

<h1>&nbsp;&nbsp;&nbsp;&nbsp; 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Prerequisite Step: Add Virtual USB Storage to VM</h1>
The first step is to add a 1GB USB (virtual) storage disk to your VM. I will leave this up to you to figure out from the settings of VirtualBox/UTM/VMWare Fusion, etc. <em><sub>Hint: Google it!</sub></em>

lsblk command provides you a list of block devices registered The (virtual) USB should already be registered and given a name (e.g., /dev/sdb).

Please complete this step before you move on! Also make sure it is 1GB, or the test script will not find it.

<h1>&nbsp;&nbsp;&nbsp;&nbsp; 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Background: Linux Block IO (BIO) Implementation</h1>
This section provides a set of internal kernel functions and data structures that you can use to access Linux’s block layer from your kernel module.

<ul>
<li><a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bdev.c#L851">struct block_device *blkdev_get_by_path(…)</a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bdev.c#L851">:</a> You can use this function to open a device with certain permissions. This is required before any block operation can be performed.</li>
</ul>
<em>Example: </em>blkdev_get_by_path(“/dev/sdb”, FMODE_READ, NULL, NULL); This opens the “/dev/sda” device for reading operations.

<ul>
<li><a href="https://elixir.bootlin.com/linux/v6.6.9/source/include/linux/blk_types.h#L264"><sub>struct bio</sub></a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/include/linux/blk_types.h#L264"><sub>:</sub></a> A data structure used for Block I/O communication within Linux. You can allocate a bio using the function <a href="https://elixir.bootlin.com/linux/v6.6.9/source/include/linux/bio.h#L429">bio_alloc(..</a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/include/linux/bio.h#L429"><sub>)</sub></a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/include/linux/bio.h#L429">.</a> The bio data structure contains two important fields for your project.</li>
<li><sub>bio-&gt;bi_iter.bi_sector</sub>: Which block (also called sector in Linux) within the storage device to read from or write to.</li>
<li><sub>bio-&gt;bi_opf</sub>: Which operation to perform (e.g., REQ_OP_READ is for read).</li>
</ul>
<em>Example: </em>bio_alloc(bdevice, 1, REQ_OP_READ, GFP_NOIO);

This creates a bio device with a single buffer for reading operations on <em><sub>bdevice</sub></em>.

<em>Note: </em>After using a bio for a read/write operation, you can reset it using the function <a href="https://elixir.bootlin.com/linux/v6.6.9/A/ident/bio_reset">bio_reset(..</a><a href="https://elixir.bootlin.com/linux/v6.6.9/A/ident/bio_reset"><sub>)</sub></a><a href="https://elixir.bootlin.com/linux/v6.6.9/A/ident/bio_reset">. </a>•<a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bio.c#L1091"><sub>int bio_add_page(..)</sub></a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bio.c#L1091">:</a> Adds a kernel page to the bio. Whichever page you specify, is the page that will be used for the I/O operation.

<em>Example: </em>bio_add_page(bio, page, 512, 0);

Adds a kernel page (physical address) to <sub>bio</sub>, and specifies that the operation (read/write depending on the value of bio-&gt;bi_opf) should be of size 512 bytes. The last “0” signifies that the operation must be performed at <em><sub>page+0 </sub></em>offset. For instance, consider a read operation. The device will write contents of disk to <em><sub>page+0 </sub></em>within the kernel’s memory.

<em>Notes:</em>

<ul>
<li>512 bytes is the largest block operation supported. If you have larger than 512 bytes data to read or write, you must break it into 512 byte chunks.</li>
<li>You can get the <em>page </em>of a kernel address using <a href="https://elixir.bootlin.com/linux/v6.6.9/source/mm/vmalloc.c#L659">vmalloc_to_page(addr</a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/mm/vmalloc.c#L659"><sub>)</sub></a></li>
<li><a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bio.c#L1356"><sub>int submit_bio_wait(bio)</sub></a><a href="https://elixir.bootlin.com/linux/v6.6.9/source/block/bio.c#L1356">:</a> Submits a BIO request and waits for it to be completed. The return value will be the bytes read or written.</li>
</ul>
Pseudocode:

<table width="624">
<tbody>
<tr>
<td width="624">// Receive IOCTL call from userspace

// Copy userspace arguments into kernel_buffer (check project 2/3)

// Use Linux block abstraction to open the audit device. bdevice = blkdev_get_by_path(…);

// Allocate a BIO for use with N buffers (1 in this case) bio = bio_alloc(bdevice, 1, REQ_OP_READ, GFP_NOIO);

// Set BIO with device (not needed if you reallocate BIO each time) bio_set_dev(bio, bdevice);

// Set BIO sector (0 in this case) and operation bio-&gt;bi_iter.bi_sector = 0; bio-&gt;bi_opf = REQ_OP_READ;

// Add kernel_buffer page to BIO with its correct offset bio_add_page(bio, vmalloc_to_page(kernel_buffer), 512, page_offset);

// Submit BIO to the device driver and wait for response submit_bio_wait(bio);

// Copy kernel_buffer back to userspace (if needed)

// Return from IOCTL call
</td>
</tr>
</tbody>
</table>
1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

16

17

18

19

20

21

22

23

24

3 Task: Support Block Operations from Userspace using Kernel Module Using Linux’s Block I/O (BIO) implementation (previous section), your kernel module should support the following operations through IOCTL calls. Provided module contains skeleton code for IOCTL calls.

<ul>
<li><sub>WRITE (buffer, size): </sub>Write buffer (of length <em><sub>size</sub></em>) at the “current” offset within the USB device. Initially current offset is “0”. Each WRITE increases the offset by <em><sub>size</sub></em>.</li>
<li><sub>READ (buffer, size): </sub>Read data (of length <em><sub>size</sub></em>) from the USB device at the “current” offset into buffer. Initially current offset is “0”. Each READ increases the offset by <em><sub>size</sub></em>.</li>
<li>WRITEOFFSET (buffer, size, offset): Same as WRITE, but instead of current offset, use the provided offset. Change current offset to the provided one.</li>
<li>READOFFSET (buffer, size, offset): Same as READ, but instead of current offset, use the provided offset. Change current offset to the provided one.</li>
</ul>
<em>Note: </em>Both <em>size </em>and <em>offset </em>are in bytes.

<h1>&nbsp;&nbsp;&nbsp;&nbsp; 4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Grading Rubric</h1>
There are 100 points available for this assignment. To test your assignment, you must run the test.sh script we have provided. <em>Note: Some of these tests may take several (&lt;5) minutes. One good way to know whether the test is still running is to add prints in the module and check the kernel logs.</em>

<table width="624">
<tbody>
<tr>
<td width="624">./test.sh &lt;test&gt; &lt;operationsize&gt; &lt;count&gt; &lt;offset&gt;</td>
</tr>
</tbody>
</table>
1

<ul>
<li>test: <em>read, write, read-variable, or write-variable</em>. The code is provided under “testcases/” <sub>operationsize</sub>: The <em><sub>size </sub></em>in READ/WRITE/READOFFSET/WRITEOFFSET</li>
<li><sub>count</sub>: Number of operations to perform.</li>
<li><sub>offset</sub>: Offset for READOFFSET/WRITEOFFSET. If 0, executes READ/WRITE.</li>
</ul>
Test Case Scoring

<ul>
<li>./test.sh read (15 points)</li>
<li>./test.sh write (15 points)</li>
<li>./test.sh read-variable 512 1 0 (5 points)</li>
<li>./test.sh write-variable 512 1 0 (5 points)</li>
<li>./test.sh read-variable 512 1024 0 (5 points)</li>
<li>./test.sh write-variable 512 100000 0 (5 points) ./test.sh read-variable 2048 100000 0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (5 points) • ./test.sh write-variable 8192 10000 0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (5 points) • ./test.sh read-variable 16384 10000 0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (5 points) • ./test.sh write-variable 131072 768 0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (5 points) • ./test.sh read-variable 512 10000 131072&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (5 points) • ./test.sh write-variable 2048 10000 16384&nbsp;&nbsp; (5 points)</li>
<li>./test.sh read-variable 16384 10000 1048576 (5 points)</li>
<li>./test.sh read-variable 8192 100 134217728 (5 points) ./test.sh write-variable 8192 512 402653184 (5 points)</li>
<li>./test.sh write-variable 393216 1024 402653184 (5 points)</li>
</ul>
<h1>&nbsp;&nbsp;&nbsp;&nbsp; 5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Submission Details</h1>
Please place the following in one zip file and submit on canvas.

<ul>
<li>The <sub>kmodule </sub> Please do not submit any binaries/.ko files.</li>
<li>Output screenshots that show your code is working for each test case.</li>
<li>A README text file clearly describing the name of the members within your group and any other details you want the TAs to know.</li>
</ul>
