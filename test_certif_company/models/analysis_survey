# -*- coding: utf-8 -*-
##############################################################################
#
#    OpenERP, Open Source Management Solution
#    Copyright (C) 2018-2019 (<http://africa-performance.com>).

##############################################################################

# imports of python lib
import base64
import re
import time

# imports of openerp
import openerp
from openerp import api, fields, models # alphabetically ordered
from openerp.tools.safe_eval import safe_eval as eval
from openerp.tools.translate import _

# imports from odoo modules
from openerp.addons.website.models.website import slug
from openerp.addons.web.controllers.main import login_redirect


class Survey(models.Models):
    _name='survey.survey'

    # fields declaration of survery
    state = fields.Selection(selection=[('draft', 'Todo'),('done', 'Done'),], string='State', required=True, readonly=True, default="draft")
    sart_date = fields.Date(string="Start date of operation")
    ot_numbers = fields.Char(string="OT Numbres")
    survey_type = fields.Selection( selection=[('loco-mag ','Loco-Mag '),('stuffing boarding','Stuffing Boarding')],string='Survey Type')
    batch_numbers = fields.Char(string="Batch number")
    lot_numbers = fields.Integer(string="Lots Numbers")
    agnets_numbers = fields.Integer(string="Number of agents to perform the operation")
    marque = fields.Char(string="Marques & Ships")
    tonnage = fields.Float(string=" Tonnage")
    date_place = fields.Char(string="Date & place of Survey")
    emportage_date = fields.Date(string="Emportage Date")
    transmission_date = fields.Date(string="transmission Date of sample")
    recipient_service = fields.Char(string="Recipient Service")
    

class Analysis(models.Models):
    _name = 'analysis.analysis'

    # fields declartion of analysis
    state = fields.Selection(selection=[('draft', 'Todo'),('done', 'Done'),], string='State', required=True, readonly=True, default="draft")
    reference = fields.Integer( string="N/REF")
    folders_numbers = fields.Integer( string="Foldre Number")
    analysis_type = fields.Selection( string="Analysis Type")
    product = fields.One2many("product.templates", string="Product")
    date_time = fields.Datetime(string="Date and time of the start of the analysis")
    batch_numbers = fields.Char(string="Batch number analyzed")
    marque = fields.Char(string="Marques")
    tonnage = fields.Float(string="Tonnage (1lot=25.05 T) ")
    date_time_end = fields.Datetime(string="Date and time of the end of the analysis")
    operator_date = fields.Date(string="Date")
    operator_name = fields.Char(string="Name of the data entry operator")
    resultat_date = fields.Date(string="Date of transmission of results")

    
