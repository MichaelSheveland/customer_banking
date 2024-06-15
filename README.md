# customer_banking
Module 3 customer_banking
from Account import Account

def create_cd_account(balance, interest_rate, months):
    """Creates a CD account, calculates interest earned, and updates the account balance.

    Args:
        balance (float): The initial CD account balance.
        interest_rate (float): The APR interest rate for the CD account.
        months (int): The length of months for the CD.

    Returns:
        tuple: A tuple containing the updated CD account balance (float) and the interest earned (float).
    """
    # Create an instance of the `Account` class
    cd_account = Account(balance)

    # Calculate interest earned
    interest_earned = balance * (interest_rate / 100) * (months / 12)

    # Update the CD account balance by adding the interest earned
    updated_balance = balance + interest_earned

    # Set the updated balance using the Account class method
    cd_account.set_balance(updated_balance)

    # Return the updated balance and interest earned
    return updated_balance, interest_earned