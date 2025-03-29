import { useState } from "react";
import './App.css';
export default function ATM() {
    const [balance, setBalance] = useState(1000);
    const [amount, setAmount] = useState("");

    const handleDeposit = () => {
        const value = parseFloat(amount);
        if (!isNaN(value) && value > 0) {
            setBalance(balance + value);
            alert(`Deposited: $${value}`);
        } else {
            alert("Enter a valid amount!");
        }
        setAmount("");
    };

    const handleWithdraw = () => {
        const value = parseFloat(amount);
        if (!isNaN(value) && value > 0 && value <= balance) {
            setBalance(balance - value);
            alert(`Withdrawn: $${value}`);
        } else {
            alert("Invalid amount or insufficient balance!");
        }
        setAmount("");
    };

    return (
        <div className="flex flex-col items-center p-6 bg-gray-100 min-h-screen">
            <div className="bg-white p-6 rounded-2xl shadow-xl w-96 text-center">
                <h2 className="text-2xl font-bold mb-4">ATM Simulator</h2>
                <p className="text-lg">Account Holder: <strong>Samruddhi Vijay More</strong></p>
                <p className="text-lg">Account Type: <strong>Savings</strong></p>
                <p className="text-lg mb-4">Balance: <strong>{balance}</strong></p>
                <input
                    type="number"
                    className="border p-2 w-full rounded"
                    placeholder="Enter amount"
                    value={amount}
                    onChange={(e) => setAmount(e.target.value)}
                />
                <div className="flex justify-between mt-4">
                    <button
                        onClick={handleDeposit}
                        className="bg-green-500 text-white px-4 py-2 rounded-lg shadow-md hover:bg-green-600"
                    >
                        Deposit
                    </button>
                    <button
                        onClick={handleWithdraw}
                        className="bg-red-500 text-white px-4 py-2 rounded-lg shadow-md hover:bg-red-600"
                    >
                        Withdraw
                    </button>
                </div>
            </div>
        </div>
    );
}
