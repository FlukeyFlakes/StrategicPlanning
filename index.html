<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Guys Trip Planner</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Slate Gray & Emerald Green -->
    <!-- Application Structure Plan: The application is structured as a single-page interactive checklist. It begins with a static reference menu, followed by a dynamic grocery list. An "Add Item" form allows users to expand the list. The core interaction is checking off items, which automatically updates category subtotals and a grand total in real-time. This structure was chosen because it directly supports the primary user task (shopping) by transforming a static plan into a functional tool that provides immediate feedback on spending and progress. A reset button adds convenience. -->
    <!-- Visualization & Content Choices: The report's tables are presented as interactive HTML tables. Goal: Track shopping progress and budget, and allow for list customization. Method: Checkboxes and a form trigger JS functions. Interaction: Checking an item strikes it through and deducts its price from the totals. Adding an item via the form appends it to the correct category and updates totals, with its price being looked up from a simulated database. Justification: This provides far more utility than a static list, making the shopping trip easier to manage and adapt. Library: Vanilla JS for all interactions. No charts needed. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f1f5f9; /* slate-100 */
        }
        .card {
            background-color: white;
            border-radius: 0.75rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            overflow: hidden;
        }
        .table-header {
            background-color: #f8fafc; /* slate-50 */
        }
        .checked-row {
            text-decoration: line-through;
            color: #94a3b8; /* slate-400 */
        }
    </style>
</head>
<body class="text-slate-800">

    <div class="container mx-auto p-4 sm:p-6 lg:p-8 max-w-6xl">
        <header class="text-center mb-8">
            <h1 class="text-3xl sm:text-4xl font-bold text-slate-900">Guys Trip Planner</h1>
            <p class="text-slate-600 mt-2">The official meal, grocery, and prep list for the brisket-edition trip.</p>
        </header>

        <!-- Menu Section -->
        <div class="card mb-8">
            <h2 class="text-xl font-bold p-4 bg-slate-50 border-b">📋 The Menu</h2>
            <div class="p-4 overflow-x-auto">
                <table class="w-full text-left text-sm">
                    <thead class="font-semibold text-slate-700">
                        <tr>
                            <th class="p-2">Meal</th>
                            <th class="p-2">Friday</th>
                            <th class="p-2">Saturday</th>
                            <th class="p-2">Sunday</th>
                        </tr>
                    </thead>
                    <tbody class="text-slate-600">
                        <tr class="border-t">
                            <td class="p-2 font-semibold">Breakfast/Brunch</td>
                            <td class="p-2">☕️ Travel Snacks</td>
                            <td class="p-2">🍳 Brisket Hash & Eggs</td>
                            <td class="p-2">🍳 Scrambled Eggs, Sausage/Bacon, Toast, Fruit</td>
                        </tr>
                        <tr class="border-t">
                            <td class="p-2 font-semibold">Lunch</td>
                            <td class="p-2">🍔 Arrive & Unpack</td>
                            <td class="p-2">🥪 Leftovers</td>
                            <td class="p-2">🥪 Brisket Grilled Cheese</td>
                        </tr>
                        <tr class="border-t">
                            <td class="p-2 font-semibold">Dinner</td>
                            <td class="p-2">🌮 Brisket Tacos</td>
                            <td class="p-2">🌭 Sausages & Veggies</td>
                            <td class="p-2">👋 Trip Over!</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
        
        <!-- Grocery List Section -->
        <div class="flex justify-between items-center mb-4">
            <h2 class="text-2xl font-bold text-slate-900">🛒 Grocery List</h2>
            <button id="reset-button" class="text-sm font-semibold text-emerald-600 hover:text-emerald-800 transition-colors">Reset List</button>
        </div>
        
        <!-- Add Item Form -->
        <div class="card mb-8 p-4">
            <h3 class="text-lg font-bold mb-2">Add New Item</h3>
            <form id="add-item-form" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-4 items-end">
                <div class="lg:col-span-2">
                    <label for="item-name" class="block text-sm font-medium text-slate-700">Item Name</label>
                    <input type="text" id="item-name" class="mt-1 block w-full rounded-md border-slate-300 shadow-sm focus:border-emerald-500 focus:ring-emerald-500 sm:text-sm" required>
                </div>
                <div>
                    <label for="item-quantity" class="block text-sm font-medium text-slate-700">Quantity</label>
                    <input type="text" id="item-quantity" class="mt-1 block w-full rounded-md border-slate-300 shadow-sm focus:border-emerald-500 focus:ring-emerald-500 sm:text-sm">
                </div>
                <div>
                    <label for="item-meal" class="block text-sm font-medium text-slate-700">For Which Meal?</label>
                    <input type="text" id="item-meal" class="mt-1 block w-full rounded-md border-slate-300 shadow-sm focus:border-emerald-500 focus:ring-emerald-500 sm:text-sm">
                </div>
                <div>
                    <label for="item-category" class="block text-sm font-medium text-slate-700">Category</label>
                    <select id="item-category" class="mt-1 block w-full rounded-md border-slate-300 shadow-sm focus:border-emerald-500 focus:ring-emerald-500 sm:text-sm">
                        <option value="meat">Meat & Seafood</option>
                        <option value="produce">Produce</option>
                        <option value="dairy">Dairy & Refrigerated</option>
                        <option value="breads">Breads & Grains</option>
                        <option value="pantry">Pantry, Sides & Condiments</option>
                        <option value="drinks">Drinks & Misc.</option>
                    </select>
                </div>
                <button type="submit" class="w-full sm:col-span-2 lg:col-span-1 inline-flex justify-center rounded-md border border-transparent bg-emerald-600 py-2 px-4 text-sm font-medium text-white shadow-sm hover:bg-emerald-700 focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:ring-offset-2">Add Item</button>
            </form>
        </div>


        <div id="grocery-list" class="space-y-6">
            <!-- Meat & Seafood -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🥩 Meat & Seafood</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="meat-subtotal">41.80</span></p>
                </div>
                <table class="w-full text-sm">
                    <tbody class="divide-y divide-slate-200" data-category="meat">
                        <tr class="grocery-item" data-price="27.00">
                            <td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td>
                            <td class="p-3 font-medium">Beef Brisket</td>
                            <td class="p-3 text-slate-500">~6 lbs</td>
                            <td class="p-3 text-slate-500">Fri Dinner, Sat Breakfast, Sun Lunch</td>
                            <td class="p-3 text-right font-mono">$27.00</td>
                        </tr>
                        <tr class="grocery-item" data-price="10.00">
                            <td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td>
                            <td class="p-3 font-medium">Sausages / Hot Links</td>
                            <td class="p-3 text-slate-500">2 packs</td>
                            <td class="p-3 text-slate-500">Sat Dinner</td>
                            <td class="p-3 text-right font-mono">$10.00</td>
                        </tr>
                        <tr class="grocery-item" data-price="4.80">
                            <td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td>
                            <td class="p-3 font-medium">Breakfast Sausage or Bacon</td>
                            <td class="p-3 text-slate-500">1 pack</td>
                            <td class="p-3 text-slate-500">Sun Brunch</td>
                            <td class="p-3 text-right font-mono">$4.80</td>
                        </tr>
                    </tbody>
                </table>
            </div>

            <!-- Produce -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🍓 Produce</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="produce-subtotal">35.16</span></p>
                </div>
                <table class="w-full text-sm">
                     <tbody class="divide-y divide-slate-200" data-category="produce">
                        <tr class="grocery-item" data-price="2.50"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Onions</td><td class="p-3 text-slate-500">3 large</td><td class="p-3 text-slate-500">All Dinners, Sat Breakfast</td><td class="p-3 text-right font-mono">$2.50</td></tr>
                        <tr class="grocery-item" data-price="4.17"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Bell Peppers</td><td class="p-3 text-slate-500">3 large</td><td class="p-3 text-slate-500">Sat Breakfast, Sat Dinner</td><td class="p-3 text-right font-mono">$4.17</td></tr>
                        <tr class="grocery-item" data-price="4.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Potatoes (for hash)</td><td class="p-3 text-slate-500">1 (5 lb) bag</td><td class="p-3 text-slate-500">Sat Breakfast</td><td class="p-3 text-right font-mono">$4.00</td></tr>
                        <tr class="grocery-item" data-price="0.50"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Cilantro</td><td class="p-3 text-slate-500">1 bunch</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$0.50</td></tr>
                        <tr class="grocery-item" data-price="1.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Limes</td><td class="p-3 text-slate-500">4</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$1.00</td></tr>
                        <tr class="grocery-item" data-price="9.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Bagged Salad</td><td class="p-3 text-slate-500">3 bags</td><td class="p-3 text-slate-500">Fri/Sat Dinner, Sun Brunch</td><td class="p-3 text-right font-mono">$9.00</td></tr>
                        <tr class="grocery-item" data-price="13.99"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Premade Fruit Tray</td><td class="p-3 text-slate-500">1 large</td><td class="p-3 text-slate-500">Sun Brunch</td><td class="p-3 text-right font-mono">$13.99</td></tr>
                    </tbody>
                </table>
            </div>

            <!-- Dairy & Refrigerated -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🥛 Dairy & Refrigerated</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="dairy-subtotal">27.79</span></p>
                </div>
                <table class="w-full text-sm">
                     <tbody class="divide-y divide-slate-200" data-category="dairy">
                        <tr class="grocery-item" data-price="7.74"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Eggs</td><td class="p-3 text-slate-500">2 dozen</td><td class="p-3 text-slate-500">Sat Breakfast, Sun Brunch</td><td class="p-3 text-right font-mono">$7.74</td></tr>
                        <tr class="grocery-item" data-price="5.19"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Shredded Cheese</td><td class="p-3 text-slate-500">1 bag</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$5.19</td></tr>
                        <tr class="grocery-item" data-price="3.10"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Sliced Cheese</td><td class="p-3 text-slate-500">1 pack</td><td class="p-3 text-slate-500">Sun Lunch</td><td class="p-3 text-right font-mono">$3.10</td></tr>
                        <tr class="grocery-item" data-price="4.50"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Butter</td><td class="p-3 text-slate-500">1 box</td><td class="p-3 text-slate-500">Sun Brunch, Sun Lunch</td><td class="p-3 text-right font-mono">$4.50</td></tr>
                        <tr class="grocery-item" data-price="7.26"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Premade Guacamole</td><td class="p-3 text-slate-500">1 container</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$7.26</td></tr>
                    </tbody>
                </table>
            </div>

             <!-- Breads & Grains -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🍞 Breads & Grains</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="breads-subtotal">11.08</span></p>
                </div>
                <table class="w-full text-sm">
                     <tbody class="divide-y divide-slate-200" data-category="breads">
                        <tr class="grocery-item" data-price="3.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Corn Tortillas</td><td class="p-3 text-slate-500">1 pack</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$3.00</td></tr>
                        <tr class="grocery-item" data-price="3.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Flour Tortillas (optional)</td><td class="p-3 text-slate-500">1 pack</td><td class="p-3 text-slate-500">Sat Breakfast</td><td class="p-3 text-right font-mono">$3.00</td></tr>
                        <tr class="grocery-item" data-price="2.50"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Sliced Bread</td><td class="p-3 text-slate-500">1 loaf</td><td class="p-3 text-slate-500">Sun Lunch</td><td class="p-3 text-right font-mono">$2.50</td></tr>
                        <tr class="grocery-item" data-price="2.58"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">English Muffins or Toast</td><td class="p-3 text-slate-500">1 pack</td><td class="p-3 text-slate-500">Sun Brunch</td><td class="p-3 text-right font-mono">$2.58</td></tr>
                    </tbody>
                </table>
            </div>

            <!-- Pantry, Sides & Condiments -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🥫 Pantry, Sides & Condiments</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="pantry-subtotal">26.68</span></p>
                </div>
                <table class="w-full text-sm">
                     <tbody class="divide-y divide-slate-200" data-category="pantry">
                        <tr class="grocery-item" data-price="4.50"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Salsa</td><td class="p-3 text-slate-500">1 jar</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$4.50</td></tr>
                        <tr class="grocery-item" data-price="3.70"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Spanish Rice (microwave)</td><td class="p-3 text-slate-500">2 pouches</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$3.70</td></tr>
                        <tr class="grocery-item" data-price="3.08"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Refried Beans</td><td class="p-3 text-slate-500">2 cans</td><td class="p-3 text-slate-500">Fri Dinner</td><td class="p-3 text-right font-mono">$3.08</td></tr>
                        <tr class="grocery-item" data-price="8.30"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Premade Potato/Pasta Salad</td><td class="p-3 text-slate-500">2 containers</td><td class="p-3 text-slate-500">Sat Dinner</td><td class="p-3 text-right font-mono">$8.30</td></tr>
                        <tr class="grocery-item" data-price="3.10"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">BBQ Sauce</td><td class="p-3 text-slate-500">1 bottle</td><td class="p-3 text-slate-500">Sun Lunch</td><td class="p-3 text-right font-mono">$3.10</td></tr>
                        <tr class="grocery-item" data-price="4.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Chips</td><td class="p-3 text-slate-500">1 bag</td><td class="p-3 text-slate-500">Sun Lunch</td><td class="p-3 text-right font-mono">$4.00</td></tr>
                    </tbody>
                </table>
            </div>

            <!-- Drinks & Misc. -->
            <div class="card">
                <div class="p-4 flex justify-between items-center table-header border-b">
                    <h3 class="font-bold text-lg">🍻 Drinks & Misc.</h3>
                    <p class="font-bold text-emerald-600">Subtotal: $<span id="drinks-subtotal">82.98</span></p>
                </div>
                <table class="w-full text-sm">
                     <tbody class="divide-y divide-slate-200" data-category="drinks">
                        <tr class="grocery-item" data-price="25.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Beer (Domestic Case)</td><td class="p-3 text-slate-500">1 (24-pack)</td><td class="p-3 text-slate-500">All Weekend</td><td class="p-3 text-right font-mono">$25.00</td></tr>
                        <tr class="grocery-item" data-price="18.99"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Tito's Vodka (750ml)</td><td class="p-3 text-slate-500">1 bottle</td><td class="p-3 text-slate-500">All Weekend</td><td class="p-3 text-right font-mono">$18.99</td></tr>
                        <tr class="grocery-item" data-price="18.99"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Captain Morgan (750ml)</td><td class="p-3 text-slate-500">1 bottle</td><td class="p-3 text-slate-500">All Weekend</td><td class="p-3 text-right font-mono">$18.99</td></tr>
                        <tr class="grocery-item" data-price="20.00"><td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td><td class="p-3 font-medium">Soda/Water/Mixers</td><td class="p-3 text-slate-500">As needed</td><td class="p-3 text-slate-500">All Weekend</td><td class="p-3 text-right font-mono">$20.00</td></tr>
                    </tbody>
                </table>
            </div>
        </div>

        <!-- Grand Total -->
        <div class="mt-8 p-6 card bg-slate-800 text-white flex justify-between items-center sticky bottom-4">
            <h3 class="text-xl sm:text-2xl font-bold">Grand Total (Remaining):</h3>
            <p class="text-2xl sm:text-3xl font-bold text-emerald-400">$<span id="grand-total">225.49</span></p>
        </div>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const resetButton = document.getElementById('reset-button');
            const addItemForm = document.getElementById('add-item-form');
            const groceryList = document.getElementById('grocery-list');
            const grandTotalElement = document.getElementById('grand-total');

            const categorySubtotalElements = {
                meat: document.getElementById('meat-subtotal'),
                produce: document.getElementById('produce-subtotal'),
                dairy: document.getElementById('dairy-subtotal'),
                breads: document.getElementById('breads-subtotal'),
                pantry: document.getElementById('pantry-subtotal'),
                drinks: document.getElementById('drinks-subtotal'),
            };

            const priceDatabase = {
                "avocado": 1.50, "lime": 0.50, "onion": 1.00, "tomato": 1.25, "cilantro": 0.75,
                "jalapeno": 0.25, "chips": 4.50, "salsa": 3.50, "beer": 25.00, "brisket": 27.00,
                "sausage": 5.00, "bacon": 4.80, "eggs": 3.87, "cheese": 5.19, "bread": 2.50,
                "butter": 4.50, "potatoes": 4.00, "peppers": 1.50, "tortillas": 3.00, "guacamole": 7.26,
                "rice": 1.85, "beans": 1.54, "salad": 3.00, "fruit": 13.99, "vodka": 18.99,
                "rum": 18.99, "soda": 6.00, "water": 5.00
            };

            function getPrice(itemName) {
                const lowerCaseItemName = itemName.toLowerCase();
                for (const key in priceDatabase) {
                    if (lowerCaseItemName.includes(key)) {
                        return priceDatabase[key];
                    }
                }
                return 5.00; // Default price for unknown items
            }

            function calculateTotals() {
                let grandTotal = 0;
                const categorySubtotals = {
                    meat: 0, produce: 0, dairy: 0,
                    breads: 0, pantry: 0, drinks: 0
                };

                document.querySelectorAll('.grocery-item').forEach(itemRow => {
                    const checkbox = itemRow.querySelector('input[type="checkbox"]');
                    const price = parseFloat(itemRow.dataset.price);
                    const category = itemRow.parentElement.dataset.category;

                    if (!checkbox.checked) {
                        grandTotal += price;
                        if (category in categorySubtotals) {
                            categorySubtotals[category] += price;
                        }
                    }
                    
                    itemRow.classList.toggle('checked-row', checkbox.checked);
                });

                for (const category in categorySubtotals) {
                    if (categorySubtotalElements[category]) {
                        categorySubtotalElements[category].textContent = categorySubtotals[category].toFixed(2);
                    }
                }
                grandTotalElement.textContent = grandTotal.toFixed(2);
            }

            groceryList.addEventListener('change', (e) => {
                if (e.target.matches('.grocery-item input[type="checkbox"]')) {
                    calculateTotals();
                }
            });

            resetButton.addEventListener('click', () => {
                document.querySelectorAll('.grocery-item input[type="checkbox"]').forEach(checkbox => {
                    checkbox.checked = false;
                });
                calculateTotals();
            });

            addItemForm.addEventListener('submit', (e) => {
                e.preventDefault();

                const itemNameInput = document.getElementById('item-name');
                const itemQuantityInput = document.getElementById('item-quantity');
                const itemMealInput = document.getElementById('item-meal');
                const itemCategorySelect = document.getElementById('item-category');

                const itemName = itemNameInput.value.trim();
                const itemQuantity = itemQuantityInput.value.trim();
                const itemMeal = itemMealInput.value.trim();
                const itemCategory = itemCategorySelect.value;

                if (!itemName) return;

                const price = getPrice(itemName);

                const newRow = document.createElement('tr');
                newRow.classList.add('grocery-item');
                newRow.dataset.price = price.toFixed(2);

                newRow.innerHTML = `
                    <td class="p-3 w-10"><input type="checkbox" class="h-4 w-4 rounded border-gray-300 text-emerald-600 focus:ring-emerald-500"></td>
                    <td class="p-3 font-medium">${itemName}</td>
                    <td class="p-3 text-slate-500">${itemQuantity}</td>
                    <td class="p-3 text-slate-500">${itemMeal}</td>
                    <td class="p-3 text-right font-mono">$${price.toFixed(2)}</td>
                `;

                document.querySelector(`[data-category="${itemCategory}"]`).appendChild(newRow);

                calculateTotals();

                addItemForm.reset();
                itemNameInput.focus();
            });

            calculateTotals();
        });
    </script>

</body>
</html>

