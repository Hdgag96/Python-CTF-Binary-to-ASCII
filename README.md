# Python-CTF-Binary-to-ASCII
This is a simple python script that helps to convert binary code to ASCII text
# binary_to_ascii.py
def binary_to_ascii(binary_str):
    """
    Converts a string of 8-bit binary numbers (separated by spaces) to ASCII text.
    """
    ascii_text = ""
    # Split the binary string into individual 8-bit blocks
    for byte in binary_str.split():
        # Convert each 8-bit binary to decimal, then to ASCII
        ascii_text += chr(int(byte, 2))
    return ascii_text

# Example usage:
if __name__ == "__main__":
    # Paste your binary string here
    binary_input = """01000111 01110010 01100101 01100001 01110100 00100000 01110111 01101111 01110010 01101011 00100001 
    00100000 01010100 01101000 01100001 01110100 00100000 01110111 01100001 01110011 00100000 01000010 
    01100001 01110011 01100101 00100000 00110010 00101100 00100000 01100010 01100101 01110100 01110100 
    01100101 01110010 00100000 01101011 01101110 01101111 01110111 01101110 00100000 01100001 01110011 
    00100000 01100010 01101001 01101110 01100001 01110010 01111001 00101110 00100000 01001001 01110100 
   ""
    
    result = binary_to_ascii(binary_input)
    print("Decoded text:\n")
    print(result)
