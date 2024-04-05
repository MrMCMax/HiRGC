
Some notes on the global fields of HiRGC:

- tar_seq_code: The compacted data of the target file.
- ref_seq_code: The compacted data of the reference file.
- meta_data: Metadata for the first line of the FASTA file.
- line_break_vec: ?
- pos_vec: ?
- other_char_vec: ?
- loc: ?
- point: ?
- dismatched_str: ?
- min_size: ??

# Changes

Meta_data is now an std::string, not initialized in intial(), cleared in the right way in clear().

I have created a new version of initial() to use with the file mode. The other modes are more complicated and I don't know yet how they work.

In HiRGC, I flattened the two loops that read the tar file to just one while loop that reads characters in a formatted input way.

I set the arrays tar_seq_code, pos_vec, line_break_vec, n_vec, and other_char_vec to all use the size of the tar file. I changed ref_seq_code to use the size of the ref file.

The answer