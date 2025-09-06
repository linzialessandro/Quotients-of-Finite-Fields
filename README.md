# Hyperfield Additive Table Generator

This notebook contains a Python script to generate the additive table for quotient hyperfields arising as GF(p^k) / G_d, where G_d is the multiplicative subgroup of GF(p^k) of order d.

Find it up to date at this Google Colab [link](https://colab.research.google.com/drive/1gdHw9UruLS6vTVjdZFO1aDp8BThbmLrv?usp=sharing).

## NEWS

- Found a nice paper and optimized the isomorphism check algorithm. Google Colab notebook with optimized algorithm [here](https://drive.google.com/file/d/16l5u-434du6FGwnNqP0fejiPqypQnL85/view?usp=sharing).


## Requirements

- Python 3.6+
- pandas (`pip install pandas`)
- galois (`pip install galois`)

## Usage

1.  **Install dependencies:** If you haven't already, run the cell with `pip install galois`. pandas is usually pre-installed in Colab.
2.  **Run the main function:** Execute the code cell containing the script. The `main()` function will prompt you to enter:
    *   A prime number `p`.
    *   An integer `k >= 1`.
    *   A divisor `d` of `p^k - 1`.
3.  **View the output:** The script will print the additive hyperoperation table for the specified quotient hyperfield as a pandas DataFrame. It will also print the characteristic and c-characteristic of the hyperfield.

## How it Works

The script utilizes the `galois` library to construct the finite field GF(p^k). It then finds a primitive element and constructs the multiplicative subgroup of order `d`. Coset representatives of GF(p^k)^*/G_d are determined, and the additive hyperoperation arising by Krasner's quotient construction is computed for all pairs of cosets (including the zero element).

## License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) file for details.
